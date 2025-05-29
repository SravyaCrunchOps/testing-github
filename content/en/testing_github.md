Yes, using a cron job (or webhook if you need real-time) is a good approach. A suggested pipeline:

Sync docs: git pull or git submodule update.

Update FAISS index: Recompute embeddings only for changed files.

Optional: Log or notify when changes are pulled.