# 🎵 Music Track Management App

<table style="width: 100%;">
  <tr>
    <td width="50%" valign="top">
      <img src="https://github.com/user-attachments/assets/247351f9-93ff-4975-9d59-a5d5b07c1cd1" alt="Music Track Management App" width="100%" />
    </td>
    <td width="50%" valign="top" style="padding-left: 20px;">
      <h2>Music Hive</h2>
      <p>
        A modern frontend application for managing music tracks, originally developed for the Front-End School 3.0 challenge. It has since been refined through extensive code reviews.
      </p>
      <h4>Core Features:</h4>
      <ul>
        <li><b>Full CRUD:</b> Create, edit, and delete music tracks.</li>
        <li><b>File Handling:</b> Upload audio files directly.</li>
        <li><b>Playback:</b> Listen to tracks with inline audio playback.</li>
        <li><b>Data Management:</b> Powerful search, filter, and sort functionalities.</li>
      </ul>
      <p>
        <a href="https://skillicons.dev">
          <img src="https://skillicons.dev/icons?i=nextjs,ts,react,graphql,tailwind" />
        </a>
      </p>
    </td>
  </tr>
</table>

<br>

## 🎵 Features

| ✨ Feature                      | ✅ Core Feature       | 🌟 Extra Feature       | 💬 Description |
|-------------------------------|-----------------------|------------------------|----------------|
| 🎼 Create Track (Without Audio) | <div align="center">✅</div> |                        | Modal for metadata input, optional cover image (with validation), metadata saved independently of audio |
| ✏️ Edit Track Metadata          | <div align="center">✅</div> |                        | Pre-filled edit modal, automatically updates the track list |
| 🎧 Upload Track Audio           | <div align="center">✅</div> |                        | Supports `.mp3` and `.wav`, validates type and size, replace/remove audio |
| ❌ Delete Track                 | <div align="center">✅</div> |                        | Removes from frontend/backend with confirmation dialog |
| 📜 Track List View              | <div align="center">✅</div> |                        | Paginated, sortable, debounced filtering, inline single-audio playback |
| 🔥 Bulk Delete                  |                        | <div align="center">✅</div> | Select and delete multiple tracks at once |
| ⚡ Optimistic UI Updates        |                        | <div align="center">✅</div> | Instant UI feedback before backend confirmation |
| 📈 Waveform Visualization       |                        | <div align="center">✅</div> | Shows waveform for currently playing track |
| 📡  SRR and SSG                 |                        | <div align="center">✅</div> | SSR implemented for the /tracks page and SSG added for individual track pages /tracks/[id]|


<br>

## 🖼️ Music Track Management App Gallery

This gallery showcases the **core functionality**, **interactive modals**, and overall **UX/UI** of the Music Track Management App. It includes examples of creating and editing tracks, uploading audio, using the audio player, applying filters, and managing the deletion process.

      
<table>
  <tr>
    <td align="center"><b>Create/Edit Track Details</b></td>
    <td align="center"><b>Manage Audio File</b></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/b92eab65-0866-45cc-9c66-2374d9fb2883" alt="Main track list view with filters and audio player." width="100%" /></td>
    <td><img src="https://github.com/user-attachments/assets/c940e73c-5611-4347-9c1c-ba59321eb830" alt="Modal for creating a new track with metadata and cover image upload." width="100%" /></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><b>Bulk Delete with Search and Sort Options</b></td>
  </tr>
  <tr>
    <td colspan="2"><img src="https://github.com/user-attachments/assets/58ebdc2c-cee1-46c7-94e3-87f57f0078da" alt="Demonstration of selecting multiple tracks for bulk deletion." width="100%" /></td>
  </tr>
</table>

<br>

## ⚡ Performance & Optimizations

Performance and accessibility were key priorities. The following optimizations were implemented to improve user experience:

-   **Optimized Image Loading**: Implemented strategies to reduce image-related delays and prevent layout shifts (CLS).
-   **Reduced Render-Blocking Resources**: Minimized render-blocking delays to significantly improve the Largest Contentful Paint (LCP) metric.
-   **Enhanced Accessibility**: Added meaningful, accessible names to all interactive elements like buttons and links.
-   **Back-Forward Cache (bfcache)**: Ensured WebSocket connections are properly closed on navigation to allow the browser to use `bfcache` for instant back/forward navigations.
   
  ![Performance](https://github.com/user-attachments/assets/cef34987-2d0c-4acf-ad3a-58df06852a4c)
  
  <br>
  
## 📦 Build
The app uses a **hybrid rendering strategy** to optimize performance and flexibility. The homepage and error page are **statically generated** for fast load times. The `/tracks` route is **server-side rendered** to handle dynamic logic or authentication. Individual track pages (`/tracks/[id]`) are **statically generated at build time**, providing excellent performance and SEO benefits.

 ![Build](https://github.com/user-attachments/assets/7448aa12-077f-4532-bfb0-cf7eb32de2c9)
  

<br>

## 🚀 Getting Started

Follow these steps to set up and run the project locally:

### 1. Clone the repository

```bash
git clone https://github.com/serhiidankovych/front-end-school-3-0-serhiidankovych.git
cd front-end-school-3-0-serhiidankovych
```

### 2. Install dependencies

Make sure you have [Node.js](https://nodejs.org/) installed.

Then install dependencies:

```bash
npm install
# or
yarn
# or
pnpm install
```

### 3. Run the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

The app should now be running at [http://localhost:3000](http://localhost:3000)

<br>

## 🧪 DEV Commands

| Task                | Command                   |
| ------------------- | ------------------------- |
| ✅ Unit Tests        | `npm run test`            |
| 🧪 End-to-End Tests | `npm run test:e2e`        |
| 🧹 Lint Code        | `npm run lint`            |
| 🛠️ Auto-fix Lint   | `npm run lint:fix`        |
| 📚 Storybook        | `npm run storybook`       |
| 📦 Build Storybook  | `npm run build-storybook` |


<br>

## 🎓 Final Mentor Feedback & Key Learnings

This project was improved through detailed mentor and peer code reviews. The final feedback below highlights strengths and key areas of growth.

<details>
  <summary><strong>Click to view the full review and key takeaways</strong></summary>

  <p><strong>Mentor's Comment:</strong> "A good, clean, and well-structured project!"</p>

  <h4>Key Strengths:</h4>
  <ul>
    <li>✅ <strong>Excellent Typing & Validation:</strong> Great use of Zod for robust data validation.</li>
    <li>✅ <strong>Clear Folder Structure:</strong> The project's architecture is intuitive and easy to navigate.</li>
    <li>✅ <strong>Reusable UI Components:</strong> Well-designed, reusable components built with best practices.</li>
    <li>✅ <strong>Comprehensive Testing:</strong> Strong test coverage across unit, integration, and E2E tests.</li>
    <li>✅ <strong>Modern Stack:</strong> Correct implementation of Next.js App Router and GraphQL.</li>
  </ul>

  <h4>Areas for Improvement & Learnings:</h4>
  <ul>
    <li>📝 <strong>Component Refactoring:</strong> Learned the importance of splitting large components like <code>TracksPageContent</code> for better readability and maintenance.</li>
    <li>📝 <strong>Semantic HTML:</strong> Gained a deeper understanding of using semantic tags (<code>nav > ul > li</code>) for better SEO and accessibility.</li>
    <li>📝 <strong>API Structure:</strong> Identified opportunities to separate API interaction methods into different files for better organization.</li>
  </ul>

  <p>This feedback was invaluable for refining the codebase and strengthening my development practices.</p>
</details>

<img width="1220" height="851" alt="image" src="https://github.com/user-attachments/assets/6151f8c8-be77-4c15-9c4f-8c10677dc22b" />



