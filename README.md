# מרכז הדוחות — אתר דוחות רב-לקוחות

אתר סטטי המארח את הדוחות הדיגיטליים של לקוחות הסוכנות. כל לקוח מקבל אזור (hub) משלו תחת נתיב ייעודי, כך שלקוחות אינם נחשפים זה לדוחות של זה.

## מבנה
```
public/
  index.html                      # נחיתה (דובדבן ביצוע)
  assets/duvdevan-logo.png        # לוגו דובדבן
  duvdevan/
    index.html                    # hub דובדבן
    may-2026/index.html           # דוח מאי 2026
  hair-cosmetics/
    index.html                    # hub הייר קוסמטיקס
    apr-may-2026/index.html       # דוח אפריל–מאי 2026 (Meta + Google)
```

## הוספת לקוח חדש
1. צרו תיקייה: `public/<client-slug>/` עם `index.html` (hub) משלו.
2. הוסיפו דוחות תחת `public/<client-slug>/<period>/index.html`.
3. מסרו ללקוח את הקישור הישיר ל-`/<client-slug>/`.

## הוספת דוח חדש ללקוח קיים
1. צרו תיקייה: `public/<client-slug>/<period>/`
2. העתיקו `index.html` מדוח קיים ועדכנו נתונים.
3. הוסיפו כרטיס חדש ל-hub של הלקוח.
4. פרסו מחדש: `vercel --prod`.

## פריסה ל-Vercel
```bash
vercel          # תצוגה מקדימה (preview)
vercel --prod   # פרודקשן
```
האתר סטטי לחלוטין (HTML/CSS/JS) — ללא תהליך build.
