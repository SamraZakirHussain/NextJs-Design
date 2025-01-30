Project Deployment Summary – Steps Taken & Issues Resolved  

Steps I Took for Deployment: 
1. Updated API Token Name Locally  
   - Changed the API token name in the local `.env` file.  
   - Ensured it followed naming rules (only letters, digits, and underscores).  

2. Pushed Changes to GitHub**  
   - Committed and pushed the updated `.env` file name (without exposing the actual token).  
   - Faced an issue where Git rejected the push due to remote changes.  

3. Resolved Git Push Issue  
   - Used `git pull origin main` to fetch the latest changes.  
   - Merged them locally, then pushed the updates successfully.  

4. Checked Vercel Environment Variables  
   - Sign Up to Vercel Dashboard and updated the environment variables.  
   - Added the correct API token (since `.env` files are not pushed to Git).  

5. Deployed on Vercel  
   - Verified automatic deployment triggered by the Git push.  
   - Deployment logs showed an error due to missing API version in the request URL.  

6. Fixed Sanity API Issue  
   - Manually added the API version in the local project.  
   - Updated and pushed the fix to GitHub, which retriggered deployment.  

7. Resolved CORS & Credentials Error  
   - Realized Sanity does not automatically update CORS settings after deployment.  
   - Manually added Vercel's domain in Sanity CORS settings under project settings.  
   - Checked if credentials were allowed in API requests.  

8. Final Check & Verification  
   - Cleared browser cache and refreshed the live site.  
   - Confirmed that products were now visible on the deployed project.  

Tools & Commands Used: 
- Git Commands: `git pull origin main`, `git push origin main`  
- Vercel Dashboard: Updated env variables, monitored deployments  
- Sanity Dashboard: Fixed CORS settings  
- Browser Debugging: Checked API errors and network responses  

Issues I Faced & How I Fixed Them:

- Git Push Rejected → Fixed by pulling the latest changes first.  
- Sanity API Not Returning Products → Added missing API version.  
- CORS Blocked Requests → Allowed Vercel domain in Sanity settings.  
- Vercel Deployment were not Reflecting Changes → Verified environment variables & retriggered deployment.  

Everything is now successfully deployed and working! 
