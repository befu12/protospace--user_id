# テーフル設計

## users テーブル
| Column             | Type   | Options    |
| ------------------ | ------ | ---------- |
| name               | string | null: false |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false |
| profile            | text   | null: false |
| occupation         | text   | null: false |
| position           | text   | null: false |

## comments テーブル
| Column    | Type       | Option     |
| --------- | ---------- | ---------- |
| user      | references | null: false, foreign_key: true |
| prototype | references | null: false, foreign_key: true |
| content   | text       | null: false |

## prototypes　テーブル
| Column     | Type       | Option     |
| ---------- | ---------- | ---------- |
| user       | references | null: false, foreign_key: true |
| title      | string     | null: false |
| concept    | text       | null: false |
| catch_copy | text       | null: false |