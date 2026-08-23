# queue-board-web

A read-only phone view of a build machine's merge queue and test queue.

The machine never listens and never streams. It encrypts a small projection of its own board with
AES-256-GCM and pushes the ciphertext outbound to a secret gist; this page fetches that ciphertext and
decrypts it in the browser with a key that exists only on the paired phone. GitHub stores bytes it
cannot read, and nothing here is a service anyone can reach.

Offline-capable, no accounts, no servers of its own. Pair once with the string the publisher prints.
