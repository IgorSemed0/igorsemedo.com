
## MER (Entity Relationship Model)

### Core Tables

#### 1. Users
```sql
users
- id (PK)
- name
- email (unique)
- email_verified_at
- password
- role (admin/user)
- slug (unique)
- created_at
- updated_at
```

#### 2. About Section
```sql
abouts
- id (PK)
- title
- content (text)
- image
- slug (unique)
- locale (en/pt)
- is_active (boolean)
- created_at
- updated_at
```

#### 3. Skills Management
```sql
skill_categories
- id (PK)
- name
- description
- icon
- slug (unique)
- locale (en/pt)
- sort_order
- is_active (boolean)
- created_at
- updated_at

skills
- id (PK)
- skill_category_id (FK)
- name
- description
- proficiency_level (1-5)
- icon
- slug (unique)
- locale (en/pt)
- sort_order
- is_active (boolean)
- created_at
- updated_at
```

#### 4. Projects Management
```sql
project_categories
- id (PK)
- name
- description
- icon
- slug (unique)
- locale (en/pt)
- sort_order
- is_active (boolean)
- created_at
- updated_at

projects
- id (PK)
- project_category_id (FK)
- title
- description
- content (text)
- image
- gallery (json)
- technologies (json)
- live_url
- github_url
- slug (unique)
- locale (en/pt)
- featured (boolean)
- status (draft/published)
- sort_order
- created_at
- updated_at
```

#### 5. Milestones
```sql
milestones
- id (PK)
- title
- description
- date
- icon
- slug (unique)
- locale (en/pt)
- is_active (boolean)
- sort_order
- created_at
- updated_at
```

#### 6. Blog System (with Taxonomies)
```sql
taxonomies
- id (PK)
- name
- slug (unique)
- type (category/tag/series/collection)
- description
- locale (en/pt)
- parent_id (FK, nullable - for hierarchy)
- sort_order
- is_active (boolean)
- created_at
- updated_at

blog_posts
- id (PK)
- title
- slug (unique)
- excerpt
- content (text/markdown)
- image
- author_id (FK users)
- status (draft/published/scheduled)
- locale (en/pt)
- featured (boolean)
- reading_time (minutes)
- meta_title
- meta_description
- published_at
- created_at
- updated_at

blog_post_taxonomy (pivot table)
- id (PK)
- blog_post_id (FK)
- taxonomy_id (FK)
- created_at
- updated_at

comments
- id (PK)
- blog_post_id (FK)
- name
- email
- content
- status (pending/approved/rejected)
- ip_address
- user_agent
- parent_id (FK, nullable - for replies)
- created_at
- updated_at
```

#### 7. Footer Management
```sql
footer_categories
- id (PK)
- name
- slug (unique)
- locale (en/pt)
- sort_order
- is_active (boolean)
- created_at
- updated_at

footer_items
- id (PK)
- footer_category_id (FK)
- name
- url
- icon
- target (_self/_blank)
- slug (unique)
- locale (en/pt)
- sort_order
- is_active (boolean)
- created_at
- updated_at
```

#### 8. Contact & Newsletter
```sql
contacts
- id (PK)
- name
- email
- subject
- message
- status (new/read/replied)
- ip_address
- user_agent
- created_at
- updated_at

newsletters
- id (PK)
- email (unique)
- name (nullable)
- status (active/unsubscribed)
- subscribed_at
- unsubscribed_at
- ip_address
- created_at
- updated_at
```