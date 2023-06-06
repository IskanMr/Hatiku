# Cara run server-CRUD

1. Sebelum kita menjalankan server, jalankan npm install untuk menginstall dependency yang ada agar API berjalan dengan baik
2. Setelah selesai menginstall, jalankan perintah npm start untuk menjalankan server API.
3. Server sukses berjalan bila pada console terdapat log Database Connected.
4. Server dapat diakses pada <url/>
5. Untuk mendapatkan data dari API (GET), hanya perlu menuju <url/>/patients
6. Untuk melakukan POST, perlu menyeragamkan JSON menjadi format seperti berikut ini :
   "name": "ryan",
   "age": 18,
   "height": 165,
   "weight": 55,
   "gender": 1,
   "ap_hi": 130,
   "ap_lo": 85,
   "cholestrol": 1,
   "gluc": 1,
   "smoke": false,
   "alco": false,
   "active": true,
   "cardio": false,

setelah itu dapat dikirimkan menuju <url/>/patients

#Requirement Server Diagnosis
fastapi
experta
pandas
numpy
sklearn
uvicorn

# Cara run server-diagnosis

1. install semua dependencies
2. run command: "uvicorn apps.server-diagnosis.main:app --reload" di console. \*<url> http://127.0.0.1:8000/diagnose/

Dokumentasi path server-diagnosis:

1. <url>/ -> (GET) berisi home, message cara penggunaan.
2. <url>/diagnosis/ -> (POST) menerima JSON berisi data pengguna, dan memberikan output diagnosis.
3. <url>/retrain/ -> (POST) menarik data dari mongoDB dan meretrain model ML.

Input /diagnosis/ :
{"age":51,
"gender":1,
"height":155,
"weight":120,
"ap_hi":190,
"ap_lo":80,
"cholesterol":2,
"gluc":2,
"smoke":1,
"alco":1,
"active":1,
"racial_identity":"african",
"blood_clotting_disorder":1,
"kidney_disease":1,
"chest_pains":1,
"breathlessness":1,
"nausea":1,
"faintings":1,
"fatigue":1,
"swollen_ankles":1,
"drastic_weight_changes":1,
"bloating":1,
"loss_of_appetite":1,
"dizziness_confusion":1,
"palpitations":1,
"atrial_fibrillation":1,
"sudden_headache":1,
"sudden_lossofvision":1,
"face_dropping":1,
"numbness":1,
"speech_problem":1,
"leg_pain_cramping":1,
"burning_aching_toes":1,
"cool_feet_skin":1,
"redness_colorchanges_skin":1,
"back_pain":1,
"coughing":1,
"hoarseness":1,
"tenderness_pain_chest":1,
"sharp_sudden_pain_upperback":1,
"pain_chest_jaw_neck_arms":1,
"loss_of_consciousness":1,
"difficulty_breathing":1,
"trouble_swallowing_food":1,
"deep_constant_belly_pain":1,
"family_history_coronaryheartdisease":1,
"personal_family_history_blood_bloodvesseldisease":1
}
