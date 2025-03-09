# **Mapty - Map Your Workout 🏃‍♂️🚴‍♀️**

## **Overview**
Mapty is a **workout tracking web application** that allows users to **log running and cycling workouts** on an interactive map. It utilizes **object-oriented programming (OOP) principles in JavaScript** and stores workout data in **local storage** to persist across sessions.

## **Features**
✅ **Add running & cycling workouts** with distance, duration, and extra metrics  
✅ **Interactive map integration** using **Leaflet.js** for workout location tracking  
✅ **Automatic pace/speed calculation** based on user input  
✅ **Workout details stored in Local Storage** for persistence  
✅ **Click on a workout entry to locate it on the map**  
✅ **Dynamic UI updates** when adding/deleting workouts  
✅ **Form handling and validation** to ensure correct input  

## **Project Architecture**
This project follows an **OOP-based structure**, with classes handling different aspects of the application:

### **1. Class Workout (Base Class)**
- Handles common properties like `distance`, `duration`, `coords`, `date`, and `clicks`
- Contains methods such as `_setDescription()` and `click()`
- **Child Classes**:
  - **Running** (adds `cadence` and `pace` + `calcPace()` method)
  - **Cycling** (adds `elevationGain` and `speed` + `calcSpeed()` method)

### **2. Class App**
- Manages **state**, **event handling**, and **UI updates**
- Implements methods for:
  - Getting user position (`_getPosition()`)
  - Loading map (`_loadMap()`)
  - Creating new workouts (`_newWorkout()`)
  - Rendering workout markers (`_renderWorkoutMarker()`)
  - Storing and retrieving workouts (`_setLocalStorage()`, `_getLocalStorage()`)
  - Handling user interactions (`_showForm()`, `_hideForm()`, `_moveToPopup()`, etc.)

### **3. Event Handling Flow**
- **Page load** → Get user location & render map
- **User clicks on the map** → Show input form
- **User submits workout form** → Validate input, create workout, render UI
- **User clicks on workout entry** → Move map to corresponding location

## **Technologies Used**
- **HTML5 & CSS3** - Basic structure and styling  
- **JavaScript (ES6+ OOP)** - Core logic and object-oriented structure  
- **Leaflet.js** - Interactive map for location tracking  
- **Local Storage API** - Persisting workout data across sessions  

## **Installation & Usage**
1. **Clone the repository**
   ```sh
   git clone https://github.com/yourusername/mapty-workout.git ```
2. **Open index.html in a browser**
No extra dependencies needed—just open the file and start using the app!

**Project Screenshot**

![image](https://github.com/user-attachments/assets/49416be7-75b3-4ba6-9653-98488d6b7fd2)


**Potential Improvements**
- 🚀 Allow users to edit/delete workouts
- 🚀 Add custom workout types (e.g., swimming, hiking)
- 🚀 Implement a dark mode UI
- 🚀 Integrate with a backend for cloud storage


