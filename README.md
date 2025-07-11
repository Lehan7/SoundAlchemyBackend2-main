# Backend API

This is the backend API service built with Node.js and Express.

## Prerequisites

- Node.js >= 18.0.0
- npm or yarn package manager

## Setup

1. Clone the repository:
```bash
git clone <your-repository-url>
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Environment Variables:
Create a `.env` file in the root directory and add your environment variables:
```env
NODE_ENV=development
PORT=3000
# Add other required environment variables
```

4. Set up Google Cloud credentials:
- Place your `credentialsound.json` file in the root directory
- Make sure it's listed in .gitignore to keep it secure

## Development

To run the server in development mode:

```bash
npm run dev
```

## Production

To start the server in production mode:

```bash
npm start
```

## Deployment

This project is configured for deployment on Vercel.

### Deploying to Vercel

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

For production deployment:
```bash
npm run deploy
```

## Project Structure

- `server.js` - Main application entry point
- `public/` - Static files
- `vercel.json` - Vercel deployment configuration

## Environment Variables on Vercel

Make sure to configure your environment variables in your Vercel project settings:

1. Go to your project on Vercel
2. Navigate to Settings > Environment Variables
3. Add all required environment variables

## Important Notes

- Ensure all sensitive credentials are added as environment variables in Vercel
- The Google Cloud credentials file should be added securely through Vercel's environment variables or secrets management
- The server is configured to handle both API routes and static file serving

## API Endpoints

- `GET /api/health`: Check server health
- `POST /api/upload-profile-image`: Upload profile image
  - Requires multipart form data with 'image' file and 'userId' field

## Troubleshooting

1. **CORS Issues**
   - Verify the frontend domain is added to allowed origins
   - Check the CORS configuration in server.js

2. **Upload Issues**
   - Verify Google Drive credentials are properly set
   - Check file size limits (currently 5MB)
   - Ensure proper folder permissions in Google Drive

3. **Firebase Issues**
   - Verify all Firebase environment variables are set
   - Check Firebase project settings and permissions

## Support

For issues and support, please create an issue in the repository or contact the development team. 