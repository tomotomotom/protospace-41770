
## usersテーブル
| カラム名             | 型        | 制約                     |
|----------------------|-----------|--------------------------|
| email               | string    | NOT NULL, ユニーク制約   |
| encrypted_password  | string    | NOT NULL                |
| name                | string    | NOT NULL                |
| profile             | text      | NOT NULL                |
| occupation          | text      | NOT NULL                |
| position            | text      | NOT NULL                |

---

## prototypesテーブル
| カラム名             | 型        | 制約                     |
|----------------------|-----------|--------------------------|
| title               | string    | NOT NULL                |
| catch_copy          | text      | NOT NULL                |
| concept             | text      | NOT NULL                |
| user                | references| NOT NULL, 外部キー      |

※ 画像はActiveStorageで実装するため含まない。

---

## commentsテーブル
| カラム名             | 型        | 制約                     |
|----------------------|-----------|--------------------------|
| content             | text      | NOT NULL                |
| prototype           | references| NOT NULL, 外部キー      |
| user                | references| NOT NULL, 外部キー      |
