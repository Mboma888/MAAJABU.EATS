# 🍽️ Maajabu Restaurant Website

[![Deploy to GitHub Pages](https://github.com/yourusername/maajabu-restaurant/actions/workflows/deploy.yml/badge.svg)](https://github.com/yourusername/maajabu-restaurant/actions/workflows/deploy.yml)

> Authentic Zambian Cuisine in Luanshya - Built with React, Vite, TypeScript, and Tailwind CSS

## ⚡ Quick Start - Deploy in 5 Minutes

### 1️⃣ Upload to GitHub
- Extract the zip file
- Create a new repository on GitHub
- Upload all files to your repository
- Commit with: `Initial commit`

### 2️⃣ Enable GitHub Pages
- Go to **Settings** → **Pages**
- Source: Select **"GitHub Actions"**
- Save

### 3️⃣ Wait for Deployment
- Go to **Actions** tab
- Wait for green checkmark ✅
- Your site is live! 🎉

**📖 Full deployment guide:** See [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md)

---

## 🎯 Features

- ✨ Modern, responsive design
- 🍕 Complete menu with categories (Traditional, Chicken, Fish, Grills, Specials)
- 📱 WhatsApp ordering integration
- 🗺️ Contact information and location
- 🎨 Beautiful UI with Tailwind CSS
- ⚡ Fast performance with Vite
- 🔒 TypeScript for type safety
- 📱 Mobile-first responsive design

---

## 🛠️ Local Development

```bash
# Install dependencies
npm install

# Start dev server (http://localhost:8080)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

---

## 📁 Project Structure

```
maajabu-restaurant/
├── .github/workflows/    # GitHub Actions deployment
├── public/               # Static assets
├── src/
│   ├── components/       # React components
│   ├── pages/            # Page components
│   ├── data/             # Menu data
│   ├── contexts/         # React contexts
│   └── lib/              # Utilities
├── index.html            # Entry HTML
├── vite.config.ts        # Vite config
└── tailwind.config.ts    # Tailwind config
```

---

## 🔧 Technologies

- **Framework**: React 18
- **Build Tool**: Vite
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: Radix UI + shadcn/ui
- **Routing**: React Router
- **Icons**: Lucide React
- **Deployment**: GitHub Pages

---

## 📝 Customization

### Update Menu Items
Edit `src/data/menuData.ts`

### Change Colors
Edit `tailwind.config.ts`

### Update Contact Info
Edit `src/pages/Contact.tsx`

### Modify WhatsApp Number
Search for `260971716370` and replace with your number

---

## 🚀 Deployment

This project is configured for automatic deployment to GitHub Pages:

- **Push to `main` branch** → Automatic deploy
- **Manual trigger** → Actions tab → "Deploy to GitHub Pages" → Run workflow

---

## 📄 License

© 2024 Maajabu Restaurant. All rights reserved.

---

## 🆘 Support

Having issues? Check [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md) for detailed troubleshooting.

---

**Built with ❤️ for Maajabu Restaurant**
