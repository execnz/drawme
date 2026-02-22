# DrawMe — Landing Page

NZ Lotto & Powerball number generator landing page with waitlist.

## Deploying to AppWrite Sites

### AppWrite Console Build Settings

| Setting           | Value                  |
|-------------------|------------------------|
| Framework         | **Other**              |
| Install command   | *(leave blank)*        |
| Build command     | `npm run build`        |
| Output directory  | `dist`                 |
| Rendering         | **Static**             |

### Steps

1. Push this repo to GitHub
2. In AppWrite Console → Sites → Create Site → Connect repository
3. Select your repo and `main` branch
4. Set build settings as above
5. Click **Deploy**

### Adding Screenshots

Place your app screenshots inside an `assets/screenshots/` folder:

```
drawme-site/
├── assets/
│   └── screenshots/
│       ├── home.png
│       ├── generate.png
│       ├── history.png
│       └── profile.png
├── index.html
├── package.json
└── README.md
```

Then update each `<img src="">` in `index.html` to:
```html
src="screenshots/home.png"
src="screenshots/generate.png"
src="screenshots/history.png"
src="screenshots/profile.png"
```

### AppWrite Waitlist Collection Setup

Create a collection called `waitlist` with these fields:

| Field       | Type     | Required |
|-------------|----------|----------|
| `email`     | String   | ✅       |
| `createdAt` | String   | ✅       |

Then update the 4 constants at the top of the `<script>` block in `index.html`:

```js
const APPWRITE_ENDPOINT      = 'https://cloud.appwrite.io/v1';
const APPWRITE_PROJECT_ID    = 'YOUR_PROJECT_ID';
const APPWRITE_DATABASE_ID   = 'YOUR_DATABASE_ID';
const APPWRITE_COLLECTION_ID = 'YOUR_COLLECTION_ID';
```
