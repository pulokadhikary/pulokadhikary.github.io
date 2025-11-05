# pulokadhikary.github.io

A personal portfolio and activity feed website with secure photo upload capabilities.

## Project Structure

```
.
├── assets/              # Image storage for blog posts and feed items
├── _posts/              # Markdown blog post files (YYYY-MM-DD-title.md format)
├── admin/               # Admin panel for authorized uploads
├── static/              # Static files (CSS, JS)
├── feed.html            # Activity feed display page
├── index.html           # Main homepage
├── style.css            # Styling
└── README.md            # This file
```

## Feed & Activity System

### Overview
This website includes a daily activity feed feature that displays blog posts with embedded images. The feed is designed with security in mind:

- **Owner (You)**: Full access to upload images and create posts
- **Visitors**: View-only access to the feed and posts

### Folders

#### `/assets`
Stores all images and media used in blog posts and feed items. Only the repository owner can upload new images via the admin panel.

#### `/_posts`
Contains Markdown files for blog posts, named in the format `YYYY-MM-DD-title.md` (e.g., `2025-11-04-sample.md`). Each post can include:
- Title and metadata
- Content written in Markdown
- References to images in the `/assets` folder

### Features

1. **Daily Activity Posts**: Create and share daily updates with photos
2. **Photo Upload**: Upload images directly through the admin panel
3. **Responsive Feed**: Posts display in a chronological feed on `feed.html`
4. **Security**:
   - Only the repository owner can access the upload functionality
   - Visitors have read-only access to view posts
   - All uploads are validated and sanitized

### Creating a New Post

1. Navigate to the admin panel (admin/index.html)
2. Upload an image (saved to `/assets`)
3. Create a new post file in `/_posts` with the naming convention `YYYY-MM-DD-title.md`
4. Include the image in your post using Markdown: `![Alt text](../assets/image-name.png)`
5. Commit your changes to the repository

### Viewing the Feed

Visit `feed.html` to see all published posts in chronological order (newest first).

## Access Control

### For Repository Owner
- Access to admin panel at `admin/index.html`
- Can upload images to `/assets`
- Can create and edit posts in `/_posts`
- Can modify feed settings and styling

### For Visitors
- View access to `index.html` and `feed.html`
- Can read all published posts
- Cannot upload or modify content
- Cannot access admin panel

## How to Set Up

1. **Clone the repository**
   ```bash
   git clone https://github.com/pulokadhikary/pulokadhikary.github.io.git
   ```

2. **Verify folder structure**
   - Ensure `assets/`, `_posts/`, and `admin/` folders exist

3. **Add sample content**
   - Create a sample post in `_posts/2025-11-04-sample.md`
   - Add images to `assets/`

4. **Test locally**
   - Open `index.html` or `feed.html` in your browser
   - Or run a local server: `python -m http.server 8000`

5. **Deploy**
   - Push changes to GitHub
   - GitHub Pages will serve the static content

## Security Considerations

- **Admin Panel Access**: Protected to only the repository owner
- **Image Validation**: Uploaded images are validated for type and size
- **No Direct Database**: Uses Markdown files and static storage for simplicity
- **GitHub Permissions**: Set repository permissions to control access

## Technologies Used

- HTML5
- CSS3
- Markdown
- JavaScript (for dynamic feed loading)
- GitHub Pages (hosting)

## Future Enhancements

- [ ] Comments system with moderation
- [ ] Search functionality for posts
- [ ] Tags and categories
- [ ] Social media integration
- [ ] Analytics and insights
- [ ] Dark mode support

## License

This project is personal and private. All rights reserved.

---

*Last updated: November 4, 2025*
