In addition to pulling updates:

Rescan changed .md files only (optional optimization).

Recompute embeddings & update FAISS index.

You could wrap this into a CLI or script like:

bash
Copy
Edit
python update_k8_docs.py
Where update_k8_docs.py:

Pulls the latest from upstream.

Finds changed .md files.

Reruns embedding and vector store updates only on deltas.