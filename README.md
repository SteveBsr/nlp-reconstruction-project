#NLP Reconstruction Project

Text reconstruction and paraphrasing using NLP models

#Περιγραφή

Το έργο αφορά την ανακατασκευή και παραφραστική ενίσχυση αγγλικών κειμένων με σκοπό τη βελτίωση της κατανόησης και της ποιότητας γραφής. Περιλαμβάνει διαφορετικές τεχνικές παραφράσεων και μέτρησης ομοιότητας.

---

#Τεχνολογίες & Εργαλεία

- Python 3.12
- Poetry (για διαχείριση εξαρτήσεων)
- Jupyter Notebook (VS Code Extension)
- Transformers (Hugging Face)
- Sentence Transformers (SBERT)
- PyTorch

---

#Παραδοτέο 1

#Παραδοτέο 1Α: Παραφράσεις

Εφαρμόστηκε το μοντέλο `Vamsi/T5_Paraphrase_Paws` για την ανακατασκευή προτάσεων από δύο κείμενα. Το μοντέλο παράγει παραφρασμένες εκδοχές για κάθε πρόταση εισόδου.

# Παραδοτέο 1Β: Πολλαπλά μοντέλα

Χρησιμοποιήθηκαν τρία διαφορετικά μοντέλα:

1. T5 Paraphraser**: `Vamsi/T5_Paraphrase_Paws`
2. Summarization Model**: `facebook/bart-large-cnn`
3. Alternate T5 Paraphraser**: `ramsrigouthamg/t5_paraphraser`

# Παραδοτέο 1Γ: Ομοιότητα

Υπολογίστηκε cosine similarity για κάθε παραφρασμένη πρόταση σε σχέση με την αρχική, για όλα τα μοντέλα. Χρησιμοποιήθηκε το embedding μοντέλο `sentence-transformers/all-MiniLM-L6-v2`.

Παρατηρήσεις:

- Το paraphrase μοντέλο #1 παρήγαγε πιο πιστές και κατανοητές εκδοχές.
- Το summarization μοντέλο συνόψισε μεγάλες ενότητες και έδωσε εναλλακτικές μορφές.
- Οι μετρήσεις cosine similarity ήταν αρκετά υψηλές για καλά παραφρασμένες προτάσεις.

---

#Οδηγίες Εκτέλεσης

#Βήματα

# 1. Κλωνοποίηση
$ git clone https://github.com/SteveBsr/nlp-reconstruction-project.git
$ cd nlp-reconstruction-project

# 2. Ενεργοποίηση poetry env
$ poetry shell

# 3. Εγκατάσταση εξαρτήσεων
$ poetry install

# 4. Εκτέλεση Notebook
Ανοίξτε το paraphrasing.ipynb μέσα από το VS Code και εκτελέστε το βήμα-βήμα.
```

---

# Δομή Αρχείων

#Παραδοτέο 2

 Παραδοτέο 2Α: Μεταγλωσσική Παραφραστική Ανακατασκευή

Έγινε μετάφραση από Αγγλικά → Γαλλικά → Αγγλικά χρησιμοποιώντας το μοντέλο Helsinki-NLP/opus-mt-en-fr και Helsinki-NLP/opus-mt-fr-en. Οι μεταγλωσσικές προτάσεις παράχθηκαν αυτόματα για όλα τα κείμενα.

Παραδοτέο 2Β: Similarity

Υπολογίστηκε cosine similarity ανάμεσα στις αρχικές και τις μεταγλωσσικές παραφράσεις χρησιμοποιώντας το sentence-transformers/all-MiniLM-L6-v2.

Παρατηρήσεις:

Οι ομοιότητες ήταν κατά μέσο όρο υψηλές (> 0.80), αλλά χαμηλότερες από τα προηγούμενα μοντέλα.
Η μετάφραση είχε κάποιες αλλοιώσεις στο ύφος.

Συμπεράσματα

Η χρήση πολλαπλών μοντέλων παραφράσεων σε συνδυασμό με γλωσσική ανάλυση παρέχει μια πλούσια εικόνα της ποιότητας της ανακατασκευής. Οι μετρικές ομοιότητας και η γλωσσική συνέπεια λειτουργούν συμπληρωματικά για την αξιολόγηση του αποτελέσματος.

#Οδηγίες Εκτέλεσης

#Βήματα

# 1. Κλωνοποίηση
$ git clone https://github.com/SteveBsr/nlp-reconstruction-project.git
$ cd nlp-reconstruction-project

# 2. Ενεργοποίηση poetry env
$ poetry shell

# 3. Εγκατάσταση εξαρτήσεων
$ poetry install

# 4. Εκτέλεση Notebook
Ανοίξτε το paraphrasing.ipynb μέσα από το VS Code και εκτελέστε το βήμα-βήμα.