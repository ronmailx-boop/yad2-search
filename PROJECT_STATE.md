# Project State

## Current Focus
עמוד בית סטטי (`index.html`) לחיפוש דירות ביד2 ומעקב אישי. באוויר ב-https://dirot.vplusstudio.app (נפרס 30.10.2026). הצעד הבא: לבדוק בטלפון שהעמוד נטען ושסינוני החניה/ממ"ד נקלטים ביד2.

## Decisions
- אין סקרייפינג של יד2: האתר מוגן ע"י Radware, ועקיפה מנוגדת לתנאי השימוש. העמוד רק בונה קישורי חיפוש ופותח אותם ביד2.
- נתונים ב-localStorage בלבד (אין backend), עם ייצוא/ייבוא JSON.
- פרמטרי URL של יד2 (`maxPrice`, `parking=1`, `shelter=1` וכו') לא אומתו מול האתר — לבדוק בטלפון שהסינונים נקלטים.

## Tasks
- [x] בונה חיפוש ליד2 (מחיר, חדרים, חניה, ממ"ד, מעלית, מרפסת, מזגן, חיות)
- [x] חיפושים שמורים
- [x] רשימת מעקב אחרי מודעות עם סטטוס, הערות, סינון ומיון
- [x] ייצוא/ייבוא גיבוי
- [x] אימות פרמטרי ה-URL מול יד2: `/realestate/rent/<region>?property=1&maxPrice=&parking=1&shelter=1&elevator=1&airConditioner=1` (אושר מקישור של המשתמש)
- [x] בחירת אזור בבונה (tel-aviv-area, center-and-sharon, south, north-and-valleys — כולם אומתו מקישורים של המשתמש; או קישור אזור מיד2)
- [x] אייקון כתום #F97216 (icons/, נוצר מ-icon.svg) + manifest.json; אריח ב-my-site (apps.vplusstudio.app) מפנה ל-dirot
- [x] סינון "רק מודעות עם מחיר / עם תמונה" (`priceOnly=1`, `imageOnly=1` — אומת מקישור של המשתמש)
- [ ] שמות (slug) של שאר האזורים ביד2 — להוסיף לרשימה כשיתקבלו קישורים
- [x] שמירת קישור חיפוש שמועתק מיד2 (עוקף את הבעיה)
- [x] קבצי פריסה ל-Cloudflare Workers (`dirot` → https://dirot.vplusstudio.app, https://dirot.ronmailx.workers.dev)
- [x] Secret `CLOUDFLARE_API_TOKEN` בריפו
- [x] מיזוג ל-main (PR #1) ופריסה — הלוג הראה workers.dev + custom domain
- [ ] מסמכים משפטיים ב-docs/legal (אם העמוד יהיה ציבורי)
