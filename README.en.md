[Español](README.md) | **English**

# Get-Together Calendar [kdemos.com](https://kdemos.com)

This is a React project for organizing meetups between friends. Users can select the days they are available to meet, indicate which days they can't, and see recommendations based on other users' availability. User data is stored and processed in Firebase or through Cloudflare Pages Workers, allowing several users to interact with the same calendar.

Features
Day Selection: Users can select the days they are available (green), the days they can't (red), and the days they can make an effort (orange).
Day Recommendation: Once users have made their selection, the system suggests the days with the most availability (more greens and fewer oranges) for all users.
Persistence in Firebase or Cloudflare Workers: User preferences are stored in Firebase in real time or, alternatively, accessed through Cloudflare Pages Workers for greater security and control.
Interactive Interface: An easy-to-use interface where users can click on the calendar days to indicate their availability.
Technologies Used
React: Library for building the user interface.
Firebase: Real-time database to store user preferences.
Cloudflare Workers: To deploy a backend layer as a secure proxy between the frontend and the database.
React Router: To handle routes and navigation between the calendar screens.
CSS Grid: To display the calendar days in a visual and orderly way.
Installation
Prerequisites

Make sure you have Node.js installed on your machine.

Clone the Repository
Clone this repository to your local machine:
bash
git clone https://github.com/tu-usuario/calendario-quedadas.git
Navigate to the project directory:
bash
cd calendario-quedadas
Install the project dependencies:
bash
npm install
Environment Configuration

The project can work with three data storage modes: mock, firebase, or cloudflare.

Configure the .env file with the desired mode:

env
REACT_APP_DB_MODE=cloudflare
Firebase Configuration (firebase mode or local development)
Create a project in Firebase Console.
Enable the Firestore database.
Get your Firebase credentials (API Key, Auth Domain, etc.) and set them in a .env file:
env
REACT_APP_FIREBASE_API_KEY=TU_API_KEY
REACT_APP_FIREBASE_AUTH_DOMAIN=TU_AUTH_DOMAIN
REACT_APP_FIREBASE_PROJECT_ID=TU_PROJECT_ID
REACT_APP_FIREBASE_STORAGE_BUCKET=TU_STORAGE_BUCKET
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=TU_MESSAGING_SENDER_ID
REACT_APP_FIREBASE_APP_ID=TU_APP_ID
Start the Project

Once everything is configured, you can start the application locally:

bash
npm start

This will open the application in your browser at http://localhost:3000.

Production Deployment

This project is ready to be deployed on platforms such as Vercel, Netlify, or Cloudflare Pages.

Deploy on Cloudflare Pages (recommended mode for production)
Create an account on Cloudflare.
Connect your GitHub repository.
Configure the environment variables in the "Settings > Functions > Environment Variables" section:
FIREBASE_PROJECT_ID
FIREBASE_API_KEY
Make sure you have REACT_APP_DB_MODE=cloudflare in your environment.
Cloudflare will deploy your application and run the Workers as the backend.
Deploy on Vercel
Create an account on Vercel.
Connect your GitHub repository to Vercel.
Configure the environment variables for Firebase (apiKey, authDomain, etc.).
Set REACT_APP_DB_MODE=firebase so the frontend accesses Firebase directly.
Contributions

Contributions are welcome, and we take part in Hacktoberfest.

Start with the good first issues: each one indicates which files to touch and how to test it.
Read the contributing guide (setup in 3 commands with REACT_APP_DB_MODE=mock, no credentials).
Do you speak another language? Translating KDEMOS is a great first contribution.

English: contributions are welcome and we take part in Hacktoberfest. Check the good first issues and the contributing guide.

License

This project is under the MIT License.
