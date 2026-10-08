# 📝 MegaBlog

A full-featured blogging platform built with **React**, **Redux Toolkit** and **Appwrite**. Users can sign up, log in, write posts with a rich text editor, upload featured images, and manage their own content.

---

## ✨ Features

- 🔐 User authentication (sign up, log in, log out) powered by Appwrite
- ✍️ Create, edit and delete blog posts
- 🖋️ Rich text editor using TinyMCE
- 🖼️ Featured image upload and storage with Appwrite Storage
- 🗂️ Post status (active / inactive)
- 🛡️ Protected routes for logged-in users
- 🧠 Global state management with Redux Toolkit
- 📋 Form handling and validation with React Hook Form
- 📱 Responsive UI styled with Tailwind CSS

## 🛠️ Tech Stack

| Category | Technology |
| --- | --- |
| Frontend | React 19, Vite |
| Routing | React Router DOM |
| State Management | Redux Toolkit, React Redux |
| Backend as a Service | Appwrite (Auth, Database, Storage) |
| Rich Text Editor | TinyMCE (`@tinymce/tinymce-react`) |
| Forms | React Hook Form |
| Styling | Tailwind CSS 4 |
| HTML Rendering | html-react-parser |
| Linting | ESLint |

## 📁 Project Structure

```
MegaBlog/
├── public/
├── src/
│   ├── appwrite/              # Appwrite service layer
│   │   ├── auth.js            # Sign up, login, logout, get current user
│   │   └── config.js          # Post CRUD and file upload/delete/preview
│   ├── components/
│   │   ├── container/
│   │   │   └── Container.jsx  # Layout wrapper
│   │   ├── Footer/
│   │   │   └── Footer.jsx
│   │   ├── Header/
│   │   │   ├── Header.jsx
│   │   │   └── LogoutBtn.jsx
│   │   ├── post-form/
│   │   │   └── PostForm.jsx   # Form used to create and edit posts
│   │   ├── AuthLayout.jsx     # Protected route wrapper
│   │   ├── Button.jsx
│   │   ├── Input.jsx
│   │   ├── Login.jsx
│   │   ├── Logo.jsx
│   │   ├── PostCard.jsx
│   │   ├── RTE.jsx            # TinyMCE rich text editor
│   │   ├── Select.jsx
│   │   ├── Signup.jsx
│   │   └── index.js           # Barrel file for component exports
│   ├── conf/
│   │   └── conf.js            # Reads environment variables
│   ├── pages/
│   │   ├── AddPost.jsx
│   │   ├── AllPosts.jsx
│   │   ├── EditPost.jsx
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Post.jsx
│   │   └── Signup.jsx
│   ├── store/
│   │   ├── authSlice.js       # Auth state (Redux Toolkit slice)
│   │   └── store.js           # Redux store setup
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx               # App entry point and router setup
├── .env.sample                # Template for environment variables
├── .gitignore
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
├── README.md
└── vite.config.js
```

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- npm
- An [Appwrite](https://appwrite.io/) project with a database, collection and storage bucket
- A [TinyMCE](https://www.tiny.cloud/) API key (if your setup uses one)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Sayan161005/MegaBlog.git
   cd MegaBlog
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**

   Create a `.env` file in the project root (use `.env.sample` as a reference):

   ```env
   VITE_APPWRITE_URL=your_appwrite_endpoint
   VITE_APPWRITE_PROJECT_ID=your_project_id
   VITE_APPWRITE_DATABASE_ID=your_database_id
   VITE_APPWRITE_COLLECTION_ID=your_collection_id
   VITE_APPWRITE_BUCKET_ID=your_bucket_id
   ```

   > ⚠️ Never commit your real `.env` file. It is already listed in `.gitignore`.

4. **Start the development server**

   ```bash
   npm run dev
   ```

   The app will be available at `http://localhost:5173`.

## 📜 Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server |
| `npm run build` | Create a production build in `dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint on the project |

## 🗄️ Appwrite Setup

1. Create a new project in the [Appwrite Console](https://cloud.appwrite.io/).
2. Add a **Web platform** and allow your local/production domain.
3. Create a **Database** and a **Collection** for posts with attributes such as `title`, `slug`, `content`, `featuredImage`, `status` and `userId`.
4. Create a **Storage Bucket** for featured images.
5. Copy the IDs into your `.env` file.

## 📚 What I Learned

- Structuring a real-world React app with reusable components
- Managing global state with Redux Toolkit
- Integrating a backend service (Appwrite) for auth, database and file storage
- Building protected routes and handling auth state
- Working with forms using React Hook Form
- Embedding a rich text editor and safely rendering its HTML output

## 📬 Contact

Made by **SAYAN SAHA** · [GitHub](https://github.com/Sayan161005) 

---

⭐ If you found this project helpful, consider giving it a star!
