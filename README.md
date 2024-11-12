

שלב ראשון - הרצת סביבת עבודה

python3 -m venv venv
או
python -m venv venv


שלב שני - להכנס לתוך סביבת העבודה, פקודה להפעלה ב WINDOWS:

.venv\Scripts\activate

שלב שלישי - הכנת דרישות לסביבת עבודה (למשל pydantic)

pip install -r requirements.txt

שלב רביעי - הרמת ה DB נניח  docker:

אפשר באמצעות פקודה או כפתור הפליי שהפייתון מציע.
docker-compose up -d --build









שלב חמישי - הרמת ויזואליזציה של ה SQL (beekeeper)fff







uvicorn main:app --reload

 uvicorn main:app --reload

ChatGPT
הפקודה uvicorn main:app --reload היא פקודת שורת פקודה להרצת אפליקציה שנכתבה באמצעות מסגרת ה-Web FastAPI, באמצעות השרת ASGI של Uvicorn. נפרט כל חלק של הפקודה:
1. Uvicorn:
Uvicorn הוא שרת ASGI (Asynchronous Server Gateway Interface) קל משקל ומהיר ל-Python. שרת ASGI מאפשר לך להריץ אפליקציות אסינכרוניות ב-Python ותומך במסגרות כמו Starlette ו-FastAPI, שמנצלות תכונות אסינכרוניות לשיפור ביצועים.
2. main:
main: שם הקובץ Python (ללא הסיומת .py) שבו נמצאת האפליקציה שלך.
app: האובייקט בתוך הקובץ main.py שמייצג את האפליקציה עצמה, כלומר, האינסטנס של האפליקציה שנוצר על ידי FastAPI או כל מסגרת אחרת תואמת ASGI.
3. --reload:
האופציה --reload מוסיפה את היכולת לשרת לטעון מחדש את האפליקציה באופן אוטומטי כל פעם שמתבצעת שינוי בקוד. זה מאוד שימושי בזמן פיתוח, כיוון שאינך צריך להפסיק ולהתחיל את השרת בכל פעם שאתה משנה משהו בקוד. שים לב שהשימוש ב--reload מיועד לסביבת פיתוח בלבד ולא מומלץ לשימוש בסביבת ייצור מכיוון שהוא עלול להשפיע על ביצועים ויציבות.
שימוש בפקודה:
כדי להשתמש בפקודה זו, פתח את שורת הפקודה או טרמינל והקלד את הפקודה בתיקייה שבה שוכן הקובץ main.py. זה יפעיל את השרת על הפורט המוגדר כברירת מחדל (בדרך כלל פורט 8000) אלא אם צוין אחרת בקוד או בפקודה. אם הכל תקין, אתה תוכל לגשת לאפליקציה דרך הדפדפן בכתובת http://localhost:8000.

במידה ויש שגיאה:





שלב 4: ודא שההתקנה הושלמה
בדוק שאין שאריות: לאחר שההתקנה הוסרה, חזור ל-Command Prompt והקלד python --version ו-pip --version כדי לראות אם עדיין מופיעה תגובה. אם כן, ייתכן שיש לנקות שאריות נוספות.
נקה את המשתנה Path: אם נותרו עדיינות כניסות ב-Path שלך ל-Python, יהיה עליך לנקות אותם דרך ה-'Environment Variables'.

