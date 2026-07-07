# Ops Manager Database Architecture

## مقدمة

قاعدة البيانات هي الأساس الذي يعتمد عليه نظام Ops Manager لتنظيم وربط جميع المعلومات التشغيلية.

---

# الجداول الرئيسية

## 1. Users

بيانات مستخدم النظام.

الحقول:

- id
- name
- email
- password
- role
- created_at

---

## 2. Branches

بيانات الفروع.

الحقول:

- id
- branch_name
- location
- opening_date
- manager
- status
- notes

---

## 3. Employees

بيانات الموظفين.

الحقول:

- id
- name
- job_title
- branch_id
- phone
- joining_date
- status

العلاقة:

الموظف مرتبط بفرع واحد.

---

## 4. Tasks

إدارة المهام.

الحقول:

- id
- title
- description
- priority
- status
- due_date
- assigned_to
- created_at

---

## 5. Meetings

الاجتماعات.

الحقول:

- id
- title
- date
- location
- notes
- attendees

---

## 6. Checklists

قوائم التشغيل.

الحقول:

- id
- name
- category
- branch_id
- completion_status

---

## 7. Inventory

المخزون.

الحقول:

- id
- item_name
- quantity
- minimum_quantity
- supplier
- branch_id

---

## 8. Sales

بيانات المبيعات.

الحقول:

- id
- branch_id
- date
- total_sales
- orders_count

---

## 9. Reports

التقارير.

الحقول:

- id
- report_type
- created_by
- date
- file_url

---

## 10. Notifications

التنبيهات.

الحقول:

- id
- title
- message
- type
- status
- created_at

---

# العلاقات الأساسية

Branch

⬇️

Employees

⬇️

Tasks

---

Branch

⬇️

Sales

⬇️

Analytics

---

Branch

⬇️

Inventory

⬇️

Reports

---

# ملاحظات مستقبلية

سيتم تطوير قاعدة البيانات لاحقًا لدعم:

- الذكاء الاصطناعي.
- تحليل الأداء.
- تعدد المستخدمين.
- تطبيق الجوال.
