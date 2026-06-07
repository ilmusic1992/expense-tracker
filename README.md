# 💰 מעקב הוצאות – Expense Tracker

אפליקציית PWA למעקב הוצאות אישי עם Firebase.

## התקנה על GitHub Pages

### שלב 1 – צור Repository
1. כנס ל [github.com/new](https://github.com/new)
2. שם: `expense-tracker`
3. Public ✓
4. לחץ **Create repository**

### שלב 2 – העלה את הקבצים
גרור את כל הקבצים האלו לתוך ה-repository:
- `index.html`
- `manifest.json`
- `icon-192.png`
- `icon-512.png`

או דרך command line:
```bash
git clone https://github.com/YOUR_USERNAME/expense-tracker
cd expense-tracker
# העתק את הקבצים לתיקייה
git add .
git commit -m "Initial commit"
git push
```

### שלב 3 – הפעל GitHub Pages
1. ב-repository → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** → **/ (root)**
4. לחץ **Save**
5. המתן ~2 דקות → האתר יהיה זמין בכתובת:
   `https://YOUR_USERNAME.github.io/expense-tracker`

### שלב 4 – הגדר Firebase Rules
ב-Firebase Console → Firestore → Rules:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

### שלב 5 – התקן כאפליקציה על הנייד
1. פתח את הכתובת בSafari (iOS) או Chrome (Android)
2. iOS: לחץ Share → **"Add to Home Screen"**
3. Android: לחץ תפריט → **"Install App"**

---
הנתונים מסתנכרנים אוטומטית בין כל המכשירים דרך Firebase.
