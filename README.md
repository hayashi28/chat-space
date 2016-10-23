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
   - name         :string
   
- users_groups
   - user_id      :reference
   - group_id     :reference

## Association

- message
   - belongs_to :user
   - belongs_to :group

- user
   - has_many :messages
   - has_many :groups through, :users_groups
   
- group
   - has_many :users through, :users_groups
   - has_many :messages
