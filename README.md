EMR - electronic medical records. 
База данных для электронных медицинских записей. 

Tables:
Doctors (PK - doctor_id)
Patients (PK - patient_id)
Reports (PK - report_id)
Referrals (PK - (report_id, doctor_id))
Appointments - (PK - (date_at, patient_id, doctor_id))

Процессы:
- Создание пациента внутри организации
- Пациент может записаться к врачу на определенную дату
- Составление отчета в виде какого-то описания и составление направлений к другим врачам, если это требуется