# Team Information and Problem Statement
| **Field**             | **Details**                                                  |
| --------------------- | ------------------------------------------------------------ |
| **Team Name**         | NooobMaxxin                                                  |
| **Members**           | Andreas Susanto, Choy Sheng Jie, Heng Pin Jie, Wong Jia Xuan |
| **Problem Statement** | Campus Management (Campus Safety App)                        |


# 📱 SafePal - Campus Safety App

A mobile app built by students, for students. With this app, no one walks alone — safety is instant, community-driven, and always within reach. See our pitch deck [here](https://www.canva.com/design/DAGyNozMbuA/Jep_GHaHS2MELIYElTutEw/view?utm_content=DAGyNozMbuA&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hd91fda64ba).

## Overview

Campus safety has always been a concern, especially during late hours, in isolated areas, or during emergencies where help is not instantly available.

Unlike conventional safety apps that only provide a **hotline**, **an emergency contact list**, or **a single panic button** to call someone, our solution is built around **real-time information sharing and transparency**. We believe that safety is about **speed and awareness** — the faster information flows, the safer a community becomes. That’s why our app reimagines campus safety by combining:

* Real-time incident reporting
* Community awareness and transparency
* Smart, priority-based alerts

All in one unified mobile experience where everyone contributes to safety, and everyone benefits from it.

## 🚀 Features

* **Incident Reporting**

   Report incidents instantly with **3 priority levels**:

  * *General Alert* → minor issues (lost & found, maintenance).

  * *Safety/Warning Alert* → suspicious behavior or hazards.

  * *Emergency/SOS Alert* → critical emergencies requiring immediate help.

   Attach text + images for better context.

* **Interactive Map**
   Real-time campus map with **incident icons**.

  * Automatic clustering for crowded areas (k-means).

  * Tap icons to see detailed reports.

* **Smart Notifications**
Priority-based alerts:

  * *General* → Logs only.

  * *Safety/Warning* → Nearby users + Campus Security.

  * *SOS* → Everyone + Security + Police.

* **Community Awareness**

  * See **who’s online** in real time.

  * Access a **live incident log** of today’s reports.

* **Future Features**

  * Friend activity tracking.

  * Safe walk (share your path with friends or security).

  * Indoor pathfinding (navigate inside buildings safely).

## 🧭 User Flow  

```mermaid
flowchart LR
    A([Login / Register]) --> B([🏠 Home: Map + Log])

    B --> C([📝 Report Incident])
    C --> D{{Select Priority}}

    D -->|General| E[[🟢 Save to Log]]
    D -->|Safety| F[[🟡 Notify Nearby Users + Security]]
    D -->|SOS| G[[🔴 Notify Everyone + Security + Police]]

    B --> H([👥 Check Online Users])
    B --> I([📍 Tap Incident → View Details])
    B --> J([🗒️ View Today's Incident Log])

    %% Styling
    style A fill:#d0ebff,stroke:#1c7ed6,stroke-width:2px
    style B fill:#e9fac8,stroke:#66a80f,stroke-width:2px
    style C fill:#ffe8cc,stroke:#f76707,stroke-width:2px
    style D fill:#fff3bf,stroke:#f08c00,stroke-width:2px
    style E fill:#d3f9d8,stroke:#37b24d,stroke-width:2px
    style F fill:#fff3bf,stroke:#f59f00,stroke-width:2px
    style G fill:#ffe3e3,stroke:#f03e3e,stroke-width:2px
    style H fill:#e5dbff,stroke:#5f3dc4,stroke-width:2px
    style I fill:#e7f5ff,stroke:#1c7ed6,stroke-width:2px
    style J fill:#f8f0fc,stroke:#862e9c,stroke-width:2px
```

## 📝 User Stories

* As a student, I want to report an incident with text/images so others are aware.

* As a user, I want to get notified when incidents happen nearby so I can stay safe.

* As a security guard, I want to be alerted on safety/emergency cases so I can act fast.

* As a user, I want to see today’s reports so I know what’s happening on campus.

* As a student, I want to share my path with friends (future) so I feel safe walking home.

## 📌 Product Backlog

### ✅ Must-Have (MVP)

* [ ] User Authentication (Supabase).

* [ ] Floating Incident Report Buttons (3 priority levels).

* [ ] Map Integration (with live incident markers).

* [ ] Real-Time Incident Log feed.

* [ ] Online User Counter (based on last active field).

### 💡 Nice-to-Have

* [ ] Marker clustering (k-means).

* [ ] Push notifications (priority-based).

* [ ] Tap markers → pop-up details.

* [ ] Friend activity tracking.

* [ ] Indoor pathfinding.

## 🗓️ Roadmap

### Week 1 — Core MVP

* Supabase setup (auth + DB schema)

* Authentication (login/register)

* Incident reporting (with image upload)

* Map view with live incidents

* Real-time log feed

### Week 2 — Polish & Advanced Features

* Marker clustering (k-means)

* Priority-based notifications

* Online user tracking

* Incident detail pop-ups

* UI polish + bug fixing

* Demo preparation

## ⚙️ Tech Stack

* **Frontend** → React Native (Expo).

* **Backend / DB** → Supabase (Postgres + Auth + Storage + Realtime).

* **Maps** → Mazemap API.

* **Notifications** → Expo Push Notifications / Firebase Cloud Messaging.

* **Algorithms** → k-means clustering for incidents.

* **Hosting** → Supabase + Expo EAS Build.

## ❓ FAQ / Clarifications  

**Q: Isn’t this just another emergency button app?**  
**A:** No. Traditional apps only connect you to a hotline or emergency contact. Our solution is **real-time, community-driven, and transparent**. Users don’t just push a button; they share and receive live information that helps the entire campus stay safe.  

**Q: How do you prevent spamming or false reports?**  
**A:** Each report is tied to a user account or anonymous. Reports can include images and descriptions, and are visible to all. Future improvements will add **verification mechanisms** (upvotes, admin moderation, credibility scores) or using k-means algorithm to filter false or duplicate reports.  

**Q: Will this overwhelm students with too many alerts?**  
**A:** No. Alerts are **priority-based**:  
- *General* → log only  
- *Safety* → nearby users + campus security  
- *Emergency/SOS* → everyone + security + police  
This ensures only critical situations trigger wider alerts.  

**Q: How is this different from campus security’s existing system?**  
**A:** Current systems are mostly **reactive** — they respond only after being contacted (calls, tickets, etc). Our app is **proactive and preventive**: everyone contributes to safety in real time, enabling faster responses and safer routes before risks escalate.  

**Q: What about privacy and data safety?**  
**A:** We use **Supabase authentication and role-based access control**. Location data is only tied to incident reports or optional features (like Safe Walk). Sensitive information is never exposed publicly.  

**Q: What if there’s no internet connection?**  
**A:** In the current prototype, internet is required.  

**Q: How scalable is this solution?**  
**A:** The design is **modular and cloud-based** (Supabase + React Native). It can start on a single campus and scale to multiple universities with minimal changes.  

**Q: What if students don’t use it?**  
**A:** Since it is community based, adoption is encouraged by making the app **useful beyond emergencies**:  
- Daily incident log  
- Online user visibility  
- Community-driven safety updates  
These features make it a habit, not just an emergency tool.  

**Q: How does this integrate with campus security?**  
**A:** Security guards have access to higher-priority alerts. They can use an **admin dashboard** (planned feature) to monitor reports in real time, improving coordination with students and authorities.  


## Installation

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

> NOTE:: At the moment, this repository does not have the prototype but the base code for this app. Reproducing the app below will only show you the base of React Native Expo App.

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).



## Prototype Screenshots
Too Long? Visit this instead

https://www.behance.net/gallery/234106939/CodeNection-2025-%28NoobMaxxin%29-SafePal
https://www.behance.net/gallery/234106939/CodeNection-2025-%28NoobMaxxin%29-SafePal
https://www.behance.net/gallery/234106939/CodeNection-2025-%28NoobMaxxin%29-SafePal

<img width="1080" height="1920" alt="Slide 16_9 - 8" src="https://github.com/user-attachments/assets/4aa74f16-bdc3-427a-a51b-f858b81fa92e" />
<img width="1920" height="1080" alt="Slide 16_9 - 3" src="https://github.com/user-attachments/assets/b8248422-b2c0-41e0-88c8-8d93f9e4b26f" />
<img width="1080" height="1920" alt="Slide 16_9 - 9" src="https://github.com/user-attachments/assets/692afff0-fc12-4afb-a000-cadfdf50b8fd" />
<img width="1920" height="1080" alt="Slide 16_9 - 4" src="https://github.com/user-attachments/assets/fa8e6f1b-2b96-4f39-8a28-21fb8402d03b" />
<img width="1080" height="1920" alt="Slide 16_9 - 10" src="https://github.com/user-attachments/assets/dcad71af-45a5-499f-8b93-4f710e3893c1" />
<img width="1080" height="1920" alt="Slide 16_9 - 12" src="https://github.com/user-attachments/assets/cbd8a8e7-1105-41de-93ee-39240702262d" />
<img width="1920" height="1080" alt="Slide 16_9 - 6" src="https://github.com/user-attachments/assets/fc3e124a-0a45-45cd-b773-05e590f17cdc" />
<img width="1080" height="1920" alt="Slide 16_9 - 13" src="https://github.com/user-attachments/assets/a2116931-ca1d-4520-8087-24d291ceafda" />
<img width="1920" height="1080" alt="Slide 16_9 - 7" src="https://github.com/user-attachments/assets/761d96f4-a9a9-44aa-bae5-5f2a8508c95b" />
<img width="1080" height="1920" alt="Slide 16_9 - 14" src="https://github.com/user-attachments/assets/ea242441-23fc-4844-8604-2cfcf0af63e8" />
<img width="1920" height="1080" alt="Slide 16_9 - 5" src="https://github.com/user-attachments/assets/b75e07d7-e2ba-4fef-97cf-55ab6aa35eed" />
<img width="1080" height="1920" alt="Slide 16_9 - 15" src="https://github.com/user-attachments/assets/bb6c06ce-5c67-4764-ada6-de24c7f5a7a2" />
<img width="1080" height="1920" alt="Slide 16_9 - 16" src="https://github.com/user-attachments/assets/23a53d2c-eb7b-4ae7-97ff-e1ecb5908923" />

