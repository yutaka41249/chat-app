# テーブル設計



| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false |



- has_many :room_users
- has_many :rooms, through: :room_users
- has_many :messages



| Column | Type   | Options    |
| ------ | ------ | ---------- |
| name   | string | null: false |



- has_many :room_users
- has_many :rooms, through: :room_users
- has_many :messages



| Column | Type       | Options     |
| ------ | ---------- | -------------------------------- |
| user   | references | null: false, foreign_key: true   |
| room   | references | null: false, foreign_key: true   |



- belongs_to :room
- belongs_to :user




| column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| content | string     |                                |
| user    | references | null: false, foreign_key: true |
| room    | references | null: false, foreign_key: true |


- belongs_to :room
- belongs_to :user