# README

## usersテーブル


| Column     | Type        | Option                    |
| ---------- | ----------- | ------------------------- |
| nickname   | string      | null: false               |
| encrypted  | string      | null: false               |


## Association

- has_many :posts
- has_many :comments


## postsテーブル


| Column     | Type         | Option                         |
| ---------- | ------------ | ------------------------------ |
| title      | string       | null: false                    |
| concept    | text         | null: false                    |
| user       | references   | null: false, foreign_key: true |


## Association

- belongs_to :user
- has_many :comments


## commentsテーブル


| Column     | Type         | Option                         |
| ---------- | ------------ | ------------------------------ |
| text       | text         | null: false                    |
| user       | references   | null: false, foreign_key: true |


## Association

- belongs_to :user
- belongs_to :post

ここから、グループ機能の追加や、ユーザー検索機能などを追加していく予定です。