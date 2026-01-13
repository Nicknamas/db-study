<img width="1308" height="973" alt="image" src="https://github.com/user-attachments/assets/abe74f9b-44c2-46fb-aabd-45d6af4c72b1" /><img width="1351" height="612" alt="image" src="https://github.com/user-attachments/assets/e8cfce31-255b-4e7d-bba5-96c32966feb7" /><img width="1300" height="792" alt="image" src="https://github.com/user-attachments/assets/fad1f589-779c-42e4-8b47-335e0b21e8ce" /># Лабораторная работа 1
## 21. Платный прием в поликлинике

Платный прием пациентов проводится врачами разных специальностей
(хирург, терапевт, кардиолог, офтальмолог и т.д.). Информация о враче
(ФИО, специальность, сумма за прием, процент отчисления). Информация о
пациенте (фамилия, имя, отчество, дата рождения, адрес).
Накапливается информация о приемах, где хранится дата приема.
Пациент оплачивает за прием некоторую сумму, которая устанавливается
персонально для каждого врача. За каждый прием врачу отчисляется
фиксированный процент от стоимости приема. 

**Выходные документы:**
- Список квитанций об оплате приема определенного пациента за
определенный период времени в порядке убывания дат. В квитанции
указывается информация о стоимости приема.
- Ведомость на оплату врачей за определенный период. Размер
начисляемой врачу заработной платы за каждый прием вычисляется по
формуле:
 Зарплата = Стоимость приема · Процент отчисления на зарплату.
 Из этой суммы вычитается подоходный налог, составляющий 13% от
начисленной зарплаты.

**Er-Диаграмма**
<img width="1297" height="967" alt="image" src="https://github.com/user-attachments/assets/cff148d3-c49a-4cd1-a00d-0d3688e0913e" />

# Лабораторная работа 2
# Логическая модель по диаграмее
## Сущности и связи
## Doctor (Доктор)
- id (PK) - уникальный идентификатор врача
- first_name - имя врача
- last_name - фамилия врача
- patronymic - отчество врача
- is_deleted - флаг удаления
- cost_per_appointment - стоимость приема
- deductions - удержания за прием
- specialty - специализация врача
- created_at - дата и время создания записи врача
- updated_at - дата и время обновения записи врача

## Patient (Пациент)
- id (PK) - уникальный идентификатор пациента
- first_name - имя пациента
- last_name - фамилия пациента
- patronymic - отчество пациента
- is_deleted - флаг удаления
- birthday - день рождения пациента
- address - адресс проживания пациента
- medical_record - номер медицинской карты
- created_at - дата и время создания записи врача
- updated_at - дата и время обновения записи врача

## Appointments (Прием)
- id (PK) - уникальный идентификатор приема
- doctor_id - уникальный идентификатор врача, который проводил прием
- patient_id - уникальный идентификатор пациента, у которого был прием
- description - описание приема
- reference_to_specialist - направление к другому специалисту

## Взаимосвязи (Relationships)
1. Doctors (1) -> (N) Appointments
   Один врач может относиться ко множеству приемов
2. Patients (1) -> (N) Appointments 
   Один пациент может относиться ко множеству приемов

# Физическая модель
<img width="1126" height="820" alt="image" src="https://github.com/user-attachments/assets/10e464e7-1217-436b-8bf1-9719b54b26b2" />
<img width="523" height="111" alt="image" src="https://github.com/user-attachments/assets/11030ee8-1070-4a79-ba82-4899c50c249f" />

# DDL
<img width="1223" height="1090" alt="image" src="https://github.com/user-attachments/assets/b8113d55-a787-48a5-a1de-4972f5848480" />

# Вставка данных
<img width="1146" height="405" alt="image" src="https://github.com/user-attachments/assets/484500ec-19c1-4cfb-a113-b0c46ff5ab57" />
<img width="883" height="372" alt="image" src="https://github.com/user-attachments/assets/4f1c62f9-29d3-42da-80a7-ff170575110c" />
<img width="852" height="440" alt="image" src="https://github.com/user-attachments/assets/0deb8fbf-433a-4a9b-95d0-6a9a282eb120" />
<img width="2322" height="911" alt="image" src="https://github.com/user-attachments/assets/2e6c54c8-64e3-4cc7-aa20-00b915069cbd" />

# Выходные документы
- Список квитанций об оплате приема определенного пациента за
определенный период времени в порядке убывания дат. В квитанции
указывается информация о стоимости приема.
<img width="828" height="615" alt="image" src="https://github.com/user-attachments/assets/895fdf89-09b7-4b8f-b1bb-97e37f8f80f2" />
<img width="1000" height="585" alt="image" src="https://github.com/user-attachments/assets/0dc36daa-3f2a-4f71-8eff-8bbe2fe515a8" />
- Ведомость на оплату врачей за определенный период. Размер
начисляемой врачу заработной платы за каждый прием вычисляется по
формуле:
 Зарплата = Стоимость приема · Процент отчисления на зарплату.
 Из этой суммы вычитается подоходный налог, составляющий 13% от
начисленной зарплаты.
<img width="1146" height="591" alt="image" src="https://github.com/user-attachments/assets/463a1bae-ff5f-4e32-83d6-e2c762c72286" />
<img width="1300" height="792" alt="image" src="https://github.com/user-attachments/assets/384d37bf-2c54-4a53-989a-2e1d7c128ceb" />

# Лабораторная 3

# Представления
<img width="778" height="625" alt="image" src="https://github.com/user-attachments/assets/d1a2b192-dd30-403c-8d80-fa716fe4a24d" />
<img width="1005" height="525" alt="image" src="https://github.com/user-attachments/assets/d04f3e7f-b2f2-4e8e-90ed-12fcbfd68f88" />
<img width="1210" height="630" alt="image" src="https://github.com/user-attachments/assets/8fba767f-2742-4989-8db6-5454a686186f" />

# Хранимые процедуры
<img width="1200" height="671" alt="image" src="https://github.com/user-attachments/assets/bc0e4219-afa0-4275-8360-f14ff11e30bb" />
<img width="1266" height="820" alt="image" src="https://github.com/user-attachments/assets/59fa0f4c-5318-4488-9a2c-f1ec1bd31f42" />
<img width="926" height="890" alt="image" src="https://github.com/user-attachments/assets/a2c906c8-fe80-4351-9b8c-f41b76a7c1b5" />
<img width="1123" height="562" alt="image" src="https://github.com/user-attachments/assets/36c412e3-51ba-4f5d-beab-e874ab57b1e4" />
<img width="1351" height="612" alt="image" src="https://github.com/user-attachments/assets/8aaa046b-e38a-46b8-ba95-56a9a88f78c4" />
<img width="925" height="670" alt="image" src="https://github.com/user-attachments/assets/66152391-4982-4cb9-8e2f-fd6a5c175a19" />
<img width="1321" height="788" alt="image" src="https://github.com/user-attachments/assets/34c4bec6-b6d3-498b-b9ac-e5ffdd7a3a36" />
<img width="695" height="662" alt="image" src="https://github.com/user-attachments/assets/b2b549a2-78ef-4a68-8fca-bdedfd6294e9" />
<img width="873" height="496" alt="image" src="https://github.com/user-attachments/assets/f8ddac18-f159-4530-a43e-dc147893f11a" />
<img width="1181" height="335" alt="image" src="https://github.com/user-attachments/assets/8f488142-0299-46df-9072-b93716ec97ba" />
<img width="807" height="983" alt="image" src="https://github.com/user-attachments/assets/cfd91ab4-b365-42b9-b877-122008adc4bb" />
<img width="1177" height="801" alt="image" src="https://github.com/user-attachments/assets/e7fa2c4d-4097-4573-bc3c-8455bea8d5be" />
<img width="1308" height="973" alt="image" src="https://github.com/user-attachments/assets/91f7b1ea-14d7-4928-a87a-6b5391156b8e" />










