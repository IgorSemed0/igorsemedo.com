# Project description
igorsemedo.com, is the show case as portfolio of Igor Silvino Domingos Semedo.

Will be a place where he will being posting articles about IT area, things about programming, Web Development, DevOps, DevTools, Project Management and more about tech related content.


## Features
- Per location language 
 - Home
	 - c_b: about section 
	 - crud_based(c_b): skills(tec) categories
	 - crud and category(ccy): skills itens per categories
	 - c_b: project categories
	 - ccy: projects
	 - c_b: especial milestones
	 - contact
	 - get in touch
 - Blog
	 - c_b: taxonomies
	 - c_b: blog post
	 - c_b: comments(email based)
	 - recent posts
	 - table of content aside left, 
	 - newsletter
-  Projects
	- c_b: project categories
	- ccy: project
- General
	- 0auth authentication 
	- c_b: footer categories
	- ccy: footer itens/links
- Dashboard
	- cruds management
	- user
	- crud management
	- markdown based blog post creator with aside preview 

# Project structure
## Development stack
- Zed Editor
- Laravel 12.25
- React 19.0.0(TSX)
- MySQL

## Project Structure

igorsemedo.com/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   ├── Admin/
│   │   │   │   ├── AuthController.php
│   │   │   │   ├── DashboardController.php
│   │   │   │   ├── UserController.php
│   │   │   │   ├── AboutController.php
│   │   │   │   ├── SkillCategoryController.php
│   │   │   │   ├── SkillController.php
│   │   │   │   ├── ProjectCategoryController.php
│   │   │   │   ├── ProjectController.php
│   │   │   │   ├── MilestoneController.php
│   │   │   │   ├── TaxonomyController.php
│   │   │   │   ├── BlogPostController.php
│   │   │   │   ├── CommentController.php
│   │   │   │   ├── FooterCategoryController.php
│   │   │   │   ├── FooterItemController.php
│   │   │   │   └── NewsletterController.php
│   │   │   └── Public/
│   │   │       ├── HomeController.php
│   │   │       ├── BlogController.php
│   │   │       ├── ProjectController.php
│   │   │       ├── ContactController.php
│   │   │       └── NewsletterController.php
│   │   └── Middleware/
│   │       ├── CheckRole.php
│   │       └── LocaleMiddleware.php
│   ├── Models/
│   │   ├── User.php
│   │   ├── About.php
│   │   ├── SkillCategory.php
│   │   ├── Skill.php
│   │   ├── ProjectCategory.php
│   │   ├── Project.php
│   │   ├── Milestone.php
│   │   ├── Taxonomy.php
│   │   ├── BlogPost.php
│   │   ├── Comment.php
│   │   ├── FooterCategory.php
│   │   ├── FooterItem.php
│   │   ├── Newsletter.php
│   │   └── Contact.php
│   └── Services/
│       ├── LocalizationService.php
│       ├── SlugService.php
│       └── MarkdownService.php
├── database/
│   ├── migrations/
│   │   ├── 2025_01_01_000001_create_users_table.php
│   │   ├── 2025_01_01_000002_create_abouts_table.php
│   │   ├── 2025_01_01_000003_create_skill_categories_table.php
│   │   ├── 2025_01_01_000004_create_skills_table.php
│   │   ├── 2025_01_01_000005_create_project_categories_table.php
│   │   ├── 2025_01_01_000006_create_projects_table.php
│   │   ├── 2025_01_01_000007_create_milestones_table.php
│   │   ├── 2025_01_01_000008_create_taxonomies_table.php
│   │   ├── 2025_01_01_000009_create_blog_posts_table.php
│   │   ├── 2025_01_01_000010_create_comments_table.php
│   │   ├── 2025_01_01_000011_create_footer_categories_table.php
│   │   ├── 2025_01_01_000012_create_footer_items_table.php
│   │   ├── 2025_01_01_000013_create_newsletters_table.php
│   │   ├── 2025_01_01_000014_create_contacts_table.php
│   │   └── 2025_01_01_000015_create_blog_post_taxonomy_table.php
│   └── seeders/
│       ├── DatabaseSeeder.php
│       ├── UserSeeder.php
│       └── LocalizationSeeder.php
├── resources/
│   ├── js/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Header.tsx
│   │   │   │   ├── Footer.tsx
│   │   │   │   ├── Navigation.tsx
│   │   │   │   ├── LanguageSwitcher.tsx
│   │   │   │   └── LoadingSpinner.tsx
│   │   │   └── admin/
│   │   │       ├── Sidebar.tsx
│   │   │       ├── AdminHeader.tsx
│   │   │       └── MarkdownEditor.tsx
│   │   ├── pages/
│   │   │   ├── admin/
│   │   │   │   ├── Dashboard.tsx
│   │   │   │   ├── about/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageAboutModal.tsx
│   │   │   │   │   │   └── AboutForm.tsx
│   │   │   │   │   └── Index.tsx
│   │   │   │   ├── skill-category/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageSkillCategoryModal.tsx
│   │   │   │   │   │   ├── ShowSkillCategoryModal.tsx
│   │   │   │   │   │   └── SkillCategoryForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── skill/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageSkillModal.tsx
│   │   │   │   │   │   ├── ShowSkillModal.tsx
│   │   │   │   │   │   └── SkillForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── project-category/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageProjectCategoryModal.tsx
│   │   │   │   │   │   ├── ShowProjectCategoryModal.tsx
│   │   │   │   │   │   └── ProjectCategoryForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── project/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageProjectModal.tsx
│   │   │   │   │   │   ├── ShowProjectModal.tsx
│   │   │   │   │   │   └── ProjectForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── milestone/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageMilestoneModal.tsx
│   │   │   │   │   │   ├── ShowMilestoneModal.tsx
│   │   │   │   │   │   └── MilestoneForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── taxonomy/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageTaxonomyModal.tsx
│   │   │   │   │   │   ├── ShowTaxonomyModal.tsx
│   │   │   │   │   │   └── TaxonomyForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── blog-post/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageBlogPostModal.tsx
│   │   │   │   │   │   ├── ShowBlogPostModal.tsx
│   │   │   │   │   │   ├── BlogPostForm.tsx
│   │   │   │   │   │   └── MarkdownPreview.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── comment/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageCommentModal.tsx
│   │   │   │   │   │   ├── ShowCommentModal.tsx
│   │   │   │   │   │   └── CommentForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── footer-category/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageFooterCategoryModal.tsx
│   │   │   │   │   │   ├── ShowFooterCategoryModal.tsx
│   │   │   │   │   │   └── FooterCategoryForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   ├── footer-item/
│   │   │   │   │   ├── partials/
│   │   │   │   │   │   ├── ManageFooterItemModal.tsx
│   │   │   │   │   │   ├── ShowFooterItemModal.tsx
│   │   │   │   │   │   └── FooterItemForm.tsx
│   │   │   │   │   ├── Index.tsx
│   │   │   │   │   └── Trash.tsx
│   │   │   │   └── newsletter/
│   │   │   │       ├── partials/
│   │   │   │       │   ├── ManageNewsletterModal.tsx
│   │   │   │       │   ├── ShowNewsletterModal.tsx
│   │   │   │       │   └── NewsletterForm.tsx
│   │   │   │       ├── Index.tsx
│   │   │   │       └── Trash.tsx
│   │   │   └── public/
│   │   │       ├── Home.tsx
│   │   │       ├── blog/
│   │   │       │   ├── Index.tsx
│   │   │       │   ├── Show.tsx
│   │   │       │   └── partials/
│   │   │       │       ├── BlogSidebar.tsx
│   │   │       │       ├── TableOfContents.tsx
│   │   │       │       ├── CommentSection.tsx
│   │   │       │       └── NewsletterForm.tsx
│   │   │       ├── project/
│   │   │       │   ├── Index.tsx
│   │   │       │   └── Show.tsx
│   │   │       └── Contact.tsx
│   │   ├── types/
│   │   │   ├── index.ts
│   │   │   ├── models.ts
│   │   │   └── api.ts
│   │   └── utils/
│   │       ├── api.ts
│   │       ├── helpers.ts
│   │       └── constants.ts
│   ├── css/
│   │   ├── app.css
│   │   ├── admin.css
│   │   └── components/
│   └── lang/
│       ├── en/
│       │   ├── common.php
│       │   ├── home.php
│       │   ├── blog.php
│       │   └── admin.php
│       └── pt/
│           ├── common.php
│           ├── home.php
│           ├── blog.php
│           └── admin.php
├── routes/
│   ├── web.php
│   ├── admin.php
│   ├── public.php
│   └── api.php
├── config/
│   ├── localization.php
│   └── portfolio.php
├── storage/
│   ├── app/
│   │   ├── public/
│   │   │   ├── projects/
│   │   │   ├── blog/
│   │   │   └── uploads/
│   └── logs/
├── public/
│   ├── assets/
│   │   ├── images/
│   │   ├── icons/
│   │   └── documents/
│   └── build/
├── tests/
│   ├── Feature/
│   │   ├── Admin/
│   │   └── Public/
│   └── Unit/
│       └── Models/
