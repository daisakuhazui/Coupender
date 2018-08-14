## 設計思想
- 無駄な機能は極力排除する
- とにかくシンプルな使い心地を追求する

## Model Design

# Models
- User
  - username
  - email
  - password

- Calender
  - title
  - owner_id

- Plan
  - title
  - from_date
  - till_date

# Intermediate Tables
- calender_plans
  - calender_id
  - plan_id

- calender_users
  - calender_id
  - user_id

## gems to use
- devise

## Functions
- UserはCalenderを何個も作成することが出来る
- Userはowner_idが自分のidが一致する場合にそのCalenderに他Userを招待できる
- 招待されたUserはオーナーと同じくCalender内のPlanを新規作成・編集・削除できる
- Userは自分の画面で閲覧できるCalenderのPlanを好きな色で表示させることができる
- Planをクリックすると予定の詳細が表示される
- Userは画面に表示するCalenderを選択できる、つまり非表示設定も出来る
- 画面表示のデフォルトは月単位カレンダーっぽい形
