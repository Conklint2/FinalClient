
## Functionality overview


**General functionality:**

- Authenticate users via JWT (login/signup pages + logout button on settings page)
- CRU* users (sign up & settings page - no deleting required)
- CRUD Activities
- CR*D Comments on activities (no updating required)
- GET and display paginated lists of activities
- Favorite activities
- Follow other users

**The general page breakdown looks like this:**

- Home page (URL: /#/ )
    - List of tags
    - List of activities pulled from either Feed, Global, or by Tag
    - Pagination for list of activities
- Sign in/Sign up pages (URL: /#/login, /#/register )
    - Uses JWT (store the token in localStorage)
    - Authentication can be easily switched to session/cookie based
- Settings page (URL: /#/settings )
- Editor page to create/edit activities (URL: /#/editor, /#/editor/article-slug-here )
- Article page (URL: /#/article/article-slug-here )
    - Delete article button (only shown to article's author)
    - Render markdown from server client side
    - Comments section at bottom of page
    - Delete comment button (only shown to comment's author)
- Profile page (URL: /#/profile/:username, /#/profile/:username/favorites )
    - Show basic user info
    - List of activities populated from author's created activities or author's favorited activities

