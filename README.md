# 📱 SafePal - Campus Safety App

A mobile app built by students, for students. With this app, no one walks alone — safety is instant, community-driven, and always within reach.

## Overview

Campus safety has always been a concern, especially during late hours, isolated areas, or emergencies where help is not instantly available. This project reimagines campus safety by combining **real-time incident reporting**, **community awareness**, and **smart alerts** into one unified mobile experience.

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

## Prototype Screenshots

<img width="1080" height="1920" alt="Slide 16_9 - 8" src="https://github.com/user-attachments/assets/4aa74f16-bdc3-427a-a51b-f858b81fa92e" />
<img width="1080" height="1920" alt="Slide 16_9 - 9" src="https://github.com/user-attachments/assets/692afff0-fc12-4afb-a000-cadfdf50b8fd" />
<img width="1080" height="1920" alt="Slide 16_9 - 10" src="https://github.com/user-attachments/assets/dcad71af-45a5-499f-8b93-4f710e3893c1" />
<img width="1080" height="1920" alt="Slide 16_9 - 12" src="https://github.com/user-attachments/assets/cbd8a8e7-1105-41de-93ee-39240702262d" />
<img width="1080" height="1920" alt="Slide 16_9 - 13" src="https://github.com/user-attachments/assets/a2116931-ca1d-4520-8087-24d291ceafda" />
<img width="1080" height="1920" alt="Slide 16_9 - 14" src="https://github.com/user-attachments/assets/ea242441-23fc-4844-8604-2cfcf0af63e8" />
<img width="1080" height="1920" alt="Slide 16_9 - 15" src="https://github.com/user-attachments/assets/bb6c06ce-5c67-4764-ada6-de24c7f5a7a2" />
<img width="1080" height="1920" alt="Slide 16_9 - 16" src="https://github.com/user-attachments/assets/23a53d2c-eb7b-4ae7-97ff-e1ecb5908923" />
