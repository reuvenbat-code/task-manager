# ⚡ מנהל משימות מתקדם

מערכת ניהול משימות מקיפה בעברית RTL עם GTD אינבוקס, יעדים, לוח בקרה, קאנבן, גאנט ועוד.

---

## 📁 קבצים להעלאה לגיטהב

```
index.html          ← האפליקציה המלאה (קובץ יחיד)
manifest.json       ← הגדרות PWA
sw.js               ← Service Worker (עבודה אופליין)
icons/
  icon-192.png
  icon-512.png
```

---

## 🚀 הוראות העלאה ל-GitHub Pages

### שלב 1 — צור Repository

1. היכנס ל-[github.com](https://github.com)
2. לחץ **+** ← **New repository**
3. שם: `task-manager` (או כל שם)
4. בחר **Public**
5. **אל** תסמן "Add README"
6. לחץ **Create repository**

### שלב 2 — העלה קבצים

בעמוד ה-repo לחץ **Add file** ← **Upload files**

גרור את הקבצים הבאים:
- `index.html`
- `manifest.json`
- `sw.js`

לתיקיית icons:
1. לחץ **Add file** ← **Create new file**
2. הקלד `icons/icon-192.png` — זה יצור תיקייה
3. מחק את הקובץ הריק ← העלה `icon-192.png` ו-`icon-512.png` לתוך `icons/`

לחץ **Commit changes**

### שלב 3 — הפעל GitHub Pages

1. **Settings** ← **Pages** (בסרגל שמאלי)
2. Source: **Deploy from a branch**
3. Branch: **main** / Folder: **/ (root)**
4. לחץ **Save**
5. המתן ~1 דקה ← רענן את הדף

האתר יהיה זמין בכתובת:
```
https://USERNAME.github.io/task-manager/
```

### שלב 4 — התקן כאפליקציה

**אנדרואיד Chrome:** פתח הכתובת ← ⋮ ← הוסף למסך הבית

**iOS Safari:** פתח הכתובת ← ↑ ← הוסף למסך הבית

---

## 🔄 עדכון גרסה עתידית

1. כנס ל-repo ← לחץ על `index.html`
2. לחץ ✏️ (עריכה) ← העלה קובץ חדש
3. **חשוב:** פתח את `sw.js` ← שנה `CACHE_NAME` מ-`v3` ל-`v4`
4. Commit changes

בלי שינוי ה-CACHE_NAME — הנייד ימשיך לטעון גרסה ישנה מהמטמון.

---

## 💾 גיבוי נתונים

הנתונים נשמרים ב-localStorage של הדפדפן.
לגיבוי: **הגדרות** ← **נתונים** ← **📤 ייצא JSON**
לשחזור: **הגדרות** ← **נתונים** ← **📥 ייבא JSON**

לסינכרון בין מכשירים: **הגדרות** ← **Gist סינכרון**
