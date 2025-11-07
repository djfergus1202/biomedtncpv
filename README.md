# 🚀 BioMed Research Suite - Vercel Deployment

## Quick Deploy Instructions

### Option 1: Deploy with Vercel CLI
```bash
# Install dependencies
npm install

# Install Vercel CLI globally
npm install -g vercel

# Deploy to Vercel
vercel

# For production deployment
vercel --prod
```

### Option 2: Deploy via GitHub
1. Push this code to a GitHub repository
2. Go to [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your GitHub repository
5. Click "Deploy"

## Project Structure
```
biomed-vercel/
├── api/
│   └── index.js       # Main API endpoints (serverless function)
├── public/
│   └── index.html     # Simple frontend interface
├── package.json       # Node.js dependencies
├── vercel.json        # Vercel configuration
└── README.md          # This file
```

## API Endpoints

Once deployed, your API will be available at:
- `https://your-app.vercel.app/api/health` - Health check
- `https://your-app.vercel.app/api/docking/proteins` - Get proteins
- `https://your-app.vercel.app/api/docking/ligands` - Get ligands
- `https://your-app.vercel.app/api/docking/run` - Run docking (POST)
- `https://your-app.vercel.app/api/cells/cell-lines` - Get cell lines
- `https://your-app.vercel.app/api/cells/simulate` - Run simulation (POST)

## Testing Your Deployment

Visit your deployed URL to see the frontend interface with test buttons for all API endpoints.

## Local Development
```bash
# Install Vercel CLI
npm install -g vercel

# Run locally
vercel dev

# Open http://localhost:3000
```

## Environment Variables

No environment variables required. The app runs with default settings.

## Troubleshooting

### "Not Found" Error
- Make sure `vercel.json` is present
- Check that `api/index.js` exists
- Verify the routes in `vercel.json`

### CORS Issues
- CORS is enabled for all origins by default
- Check the headers in `vercel.json`

### Function Timeout
- Default timeout is 30 seconds
- Can be adjusted in `vercel.json` under `functions`

## Support

For issues, check:
1. Vercel deployment logs: https://vercel.com/dashboard
2. Function logs: Click on your project → Functions tab
3. API health: https://your-app.vercel.app/api/health
