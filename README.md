# 🩸 LifeDrop — Blood Donation Platform

A web platform connecting blood donors with people in need, built during a hackathon and later refined into a fully functional client-side application.

## 📌 About The Project

LifeDrop helps people register as blood donors and helps those in need find available donors by blood group and location. The platform aims to reduce response time during blood shortage emergencies by making donor information easily searchable.

## 🚀 Live Demo

[View Live Site](https://tink-her-hack-3-temp-pi.vercel.app)

## ✨ Features

- 🆕 **Donor Registration** — users can register as blood donors with their name, blood group, location, and contact details
- 🔍 **Find a Donor** — search for available donors filtered by blood group and location
- 💾 **Persistent Storage** — donor data is saved in the browser using `localStorage`, so registered donors remain available across sessions
- ✅ **Real-time Feedback** — success and error messages guide the user through registration and search

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 | Styling and responsive layout |
| JavaScript (Vanilla) | Form handling, data storage, and search logic |
| Browser `localStorage` API | Client-side data persistence (no backend needed) |
| Vercel | Deployment and hosting |

## ⚙️ How It Works

This is a **frontend-only application** — there is no backend server or database. Instead, the browser's built-in `localStorage` API is used to simulate a simple database:

1. **Registering a donor**: When the "Register as Donor" form is submitted, JavaScript reads the form values, packages them into an object, and adds that object to an array stored in `localStorage` under the key `lifedrop_donors`.
2. **Finding a donor**: When the "Find a Donor" form is submitted, JavaScript retrieves the donor array from `localStorage`, filters it by matching blood group and a partial, case-insensitive match on location, and dynamically renders the matching results on the page.
3. **Data persistence**: Because `localStorage` writes directly to the browser, the donor data persists even after the page is refreshed or the browser is closed and reopened — as long as it's the same browser and device.

This approach demonstrates core front-end engineering concepts — DOM manipulation, event handling, and client-side data persistence — without requiring any server infrastructure.

## 📂 Project Structure

```
LifeDrop/
│
├── index.html          # Main application file (HTML, CSS, and JavaScript)
└── README.md            # Project documentation
```

## 🔮 Future Improvements

- Migrate from `localStorage` to a real backend (e.g., Firebase or a REST API) so donor data is shared across all users and devices, not just one browser
- Add email/SMS notifications for matched donor requests
- Add donor verification and admin moderation


## 📄 License

This project is open source and available under the [MIT License](LICENSE).
