# Vercel Deployment Guide

To get your AI features working on Vercel, you *must* configure your Environment Variables in the Vercel dashboard.

## Step 1: Add Environment Variables
1. Go to your [Vercel Dashboard](https://vercel.com/dashboard).
2. Click on your project (**smart-keyboard**).
3. Go to **Settings** -> **Environment Variables**.
4. Add the following variables:

| Variable Name | Value | Description |
| :--- | :--- | :--- |
| `GEMINI_API_KEY` | `AIzaSyDyXtGM4IIB087dMzangH_8DSzVTUsrMAw` | Your new Google Gemini API Key |
| `JWT_SECRET` | *(Any long random string)* | Used for securing API calls |
| `ALLOWED_ORIGINS` | `https://your-domain.vercel.app` | Your actual Vercel site URL |
| `MONGODB_URI` | *(Your MongoDB Atlas String)* | Only if you want database features |

## Step 2: Redeploy
After adding the variables, you must redeploy for them to take effect:
1. Go to the **Deployments** tab in Vercel.
2. Click the three dots (...) on your latest deployment.
3. Select **Redeploy**.

## Step 3: Verify
- On your website, look at the status bar.
- If it says **"Error: GEMINI_API_KEY not configured"**, verify your Step 1 settings.
- If it says **"Ready"**, your AI is working!
