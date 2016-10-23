# chat-space
====

## Database

- message
   - body         :text
   - image        :string
   - user_id      :reference
   - group_id     :reference

- user
   - name         :string
   - e-mail       :string
   - password     :string
   
- group
   - group_name   :string
   - member_name  :string
   
- users_groups
   - user_id      :reference
   - group_id     :reference

## Association

- message
   - belongs_to :user

- user
   - has_many :messages
   - has_many :groups
   
- group
   - has_many :users
