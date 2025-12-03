---
layout: essay
type: essay
title: "Design Patterns: The Hidden Architecture Behind WarriorHub"
date: 2025-12-03
published: true
labels:
  - Software Engineering
  - Design Patterns
  - ICS 314
---

<img width="350px" class="rounded float-start pe-4" src="../img/public.jpg" alt="Illustration">

## Understanding Design Patterns Through Everyday Systems

As I built out the WarriorHub project, I realized that certain design patterns naturally appeared throughout the code—patterns that show up not only in software but also in everyday environments. Design patterns aren’t strict rules. Instead, they are familiar structures that make systems easier to maintain, more predictable, and easier to reason about. Seeing them show up in WarriorHub made the project feel less like assembling isolated components and more like coordinating a thoughtful, interconnected system.

## Structural Patterns: A Restaurant with Clear Roles

One design pattern that stood out was the idea of structural architecture, which focuses on organizing a system into clear layers. The best way I can describe it is through a restaurant. In a well-run restaurant, the dining room, kitchen, and storage areas each have distinct responsibilities. The dining room is where customers place orders and interact with the service staff. The kitchen interprets those orders and prepares the meals. Meanwhile, the storage area quietly supports everything behind the scenes. WarriorHub follows this exact model. React components serve as the “dining room” that users interact with. The Next.js API routes function like the kitchen staff, taking requests and handling the logic. Prisma and PostgreSQL act as the storage system that holds ingredients—in this case, all the application’s data. The system works smoothly because these layers don’t overlap. Just as customers shouldn’t walk into the kitchen or rearrange the storage shelves, the UI never touches the database directly. This clean separation is what keeps the entire structure stable and manageable.

## Behavioral Patterns: React as a System of Sensors

Another pattern I noticed falls under behavioral design, where different parts of a system respond automatically to changes. React functions a lot like a network of building sensors. Motion sensors flip on the lights when someone enters a room, thermostats adjust when the temperature shifts, and automatic doors open when someone approaches. In WarriorHub, `useState` stores information that can change, and `useEffect` acts like a sensor that “watches” those values. When the user changes the calendar month, the app fetches new events automatically. When someone types into the search bar, the event list updates in real time. When a session changes, the “My Events” page loads the correct data. Even the image preview updates instantly when a different URL is entered. The UI adapts to internal changes without requiring manual updates, making the interface feel responsive and dynamic.

## Behavioral Patterns: Gatekeeping Through Authorization

The third major pattern in WarriorHub is also behavioral but focuses on **policy and gatekeeping logic**. This pattern controls who is allowed to do what—similar to how certain rooms in a building require keycards or how restaurants restrict kitchen access to staff only. WarriorHub checks a user’s identity and role before allowing specific actions. Only the creator of an event or an admin can edit or delete it, and some pages require a logged-in session before loading at all. These authorization checks ensure that users interact only with the features they’re permitted to access. This gatekeeping pattern keeps the application secure, prevents unauthorized data changes, and helps maintain data integrity throughout the system.

## Seeing the Architecture Behind the App

Recognizing these patterns helped me appreciate WarriorHub not just as a collection of pages and components but as a system shaped by structure and behavior. The layered architecture keeps everything organized, the reactive state updates make the interface responsive, and the authorization logic maintains security. These patterns aren’t just theoretical ideas—they’re the hidden architecture that makes the project function smoothly and predictably.

*Attribution: I used ChatGPT to help refine the organization, metaphors, and grammar of this essay.*
