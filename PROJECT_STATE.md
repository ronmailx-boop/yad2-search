# Project State

## Current Focus
עמוד בית סטטי (`index.html`) לחיפוש דירות ביד2 ומעקב אישי. הצעד הבא: מיזוג ל-main, הוספת ה-Secret `CLOUDFLARE_API_TOKEN`, ובדיקת הלוג של "Deploy to Cloudflare".

## Decisions
- אין סקרייפינג של יד2: האתר מוגן ע"י Radware, ועקיפה מנוגדת לתנאי השימוש. העמוד רק בונה קישורי חיפוש ופותח אותם ביד2.
- נתונים ב-localStorage בלבד (אין backend), עם ייצוא/ייבוא JSON.
- פרמטרי URL של יד2 (`maxPrice`, `parking=1`, `shelter=1` וכו') לא אומתו מול האתר — לבדוק בטלפון שהסינונים נקלטים.

## Tasks
- [x] בונה חיפוש ליד2 (מחיר, חדרים, חניה, ממ"ד, מעלית, מרפסת, מזגן, חיות)
- [x] חיפושים שמורים
- [x] רשימת מעקב אחרי מודעות עם סטטוס, הערות, סינון ומיון
- [x] ייצוא/ייבוא גיבוי
- [ ] אימות פרמטרי ה-URL מול יד2 בטלפון
- [x] קבצי פריסה ל-Cloudflare Workers (`dirot` → https://dirot.vplusstudio.app, https://dirot.ronmailx.workers.dev)
- [ ] Secret `CLOUDFLARE_API_TOKEN` בריפו (המשתמש)
- [ ] מיזוג ל-main ואימות הפריסה בלוג
- [ ] מסמכים משפטיים ב-docs/legal (אם העמוד יהיה ציבורי)
