# דובדבן ביצוע — מרכז הדוחות

אתר סטטי המארח את הדוחות הדיגיטליים החודשיים של חברת דובדבן ביצוע.

## מבנה
```
public/
  index.html                 # מרכז הדוחות (Hub)
  assets/duvdevan-logo.png   # לוגו רשמי
  duvdevan/
    may-2026/index.html      # דוח מאי 2026
```

## הוספת דוח חדש
1. צרו תיקייה: `public/duvdevan/<month>-<year>/`
2. העתיקו את `index.html` מדוח קיים ועדכנו נתונים.
3. הוסיפו כרטיס חדש ל-`public/index.html`.
4. פרסו מחדש: `vercel --prod`.

## פריסה ל-Vercel
```bash
vercel          # תצוגה מקדימה (preview)
vercel --prod   # פרודקשן
```
האתר סטטי לחלוטין (HTML/CSS/JS) — ללא תהליך build.
