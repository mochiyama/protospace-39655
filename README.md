# テーブル設計

## users テーブル

| colum              | Type        | Options 1   | Options 2  |
| ------------------ | ----------  | ----------- | ---------- |
| email              | string      | NOT NULL    | ユニーク制約 |
| encrypted_password | string      | NOT NULL    |            |
| name               | string      | NOT NULL    |            |
| profile            | text        | NOT NULL    |            |
| occupation         | text        | NOT NULL    |            |
| position           | text        | NOT NULL    |            |

##comments
| colum              | Type        | Options 1   | Options 2 |
| ------------------ | ----------  | ----------- | --------- |
| content            | text        | NOT NULL    |           |
| prototype          | references  | NOT NULL    | 外部キー   |
| user               | references  | NOT NULL    | 外部キー   |

##prototypes
| colum              | Type        | Options 1   | Options 2  |
| ------------------ | ----------  | ----------- | ---------- |
| title              | string      | NOT NULL    |            |
| catch_copy         | text        | NOT NULL    |            |
| concept            | text        | NOT NULL    |            |
| user               | references  | NOT NULL    | 外部キー    |