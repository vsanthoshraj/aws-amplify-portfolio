 Cloud Portfolio Website on AWS Amplify

A high-performance, fully responsive personal portfolio website using HTML, CSS, and JavaScript. Deployed with a modern DevOps workflow, **CI/CD pipeline, global CDN, HTTPS, and custom domain**,leveraging the power of **AWS Amplify** and GitHub.

---

## 
demo link using vercel because Not having enough money to host in aws   
https://santhoshrajv-portfolio.vercel.app/

---

## Project Highlights

- **CI/CD Automation:** Every code push to GitHub instantly triggers AWS Amplify to build and deploy your portfolio globally.
- **Custom Domain + SSL:** Secure, trustworthy web presence with your own domain and free, auto-renewing SSL certificate via AWS.
- **CloudFront CDN:** Blazing fast site delivery from 450+ edge locations worldwide for lowest latency.
- **Scalable Hosting:** Static website hosted on S3 for reliability, minimal cost, and instant scale as your traffic grows.
- **Monitoring:** Built-in CloudWatch metrics for usage, uptime, and error monitoring.
- **AWS Free Tier Friendly:** Most portfolios deploy and serve in the free tier with little to no cost.

---

##  Tech Stack

- Plain HTML5, CSS3, JavaScript (no frameworks needed)
- AWS Amplify (Hosting & CI/CD)
- Amazon CloudFront (CDN)
- Amazon S3 (static assets)
- Amazon Route 53 (domain)
- AWS Certificate Manager (HTTPS)
- GitHub (version control and automation)

---

##  Repository Structure

```plaintext
/
├── index.html         # Main entry file 
├── styles.css         # Main stylesheet
├── scripts.js         # main scripts
├── assets/            # Images, icons, resume, etc.
│   ├── images/
│   └── docs/
├── README.md          # This file
```

---

## 👷 How It Works (CI/CD Flow)

1. **Development:** Edit HTML, CSS, JS files locally in your code editor.
2. **Version Control:** Stage changes with `git add .`, commit with `git commit -m "message"`.
3. **GitHub Push:** Push to main branch with `git push origin main`.
4. **Build Trigger:** AWS Amplify detects changes via GitHub webhook and automatically starts the CI/CD pipeline.
5. **Build & Deploy:** Amplify builds (or simply copies for static sites) your project and deploys to Amazon S3.
6. **CDN Delivery:** Amazon CloudFront caches and serves your site globally, performing cache invalidation on every deployment.
7. **Live Updates:** Your portfolio changes go live globally within 2–3 minutes of each git push.

---

## 🌟 Key Features & Benefits

### ✅ Mobile-First Design
- Fully responsive layout works perfectly on phones, tablets, and desktops.

### ⚡ Lightning Fast Performance
- CloudFront CDN edge delivery ensures sub-second page loads worldwide.
- Average response time: < 500ms from any location.

### 🔒 Secure by Default
- HTTPS enabled with strong SSL/TLS encryption (free via AWS Certificate Manager).
- Security headers and best practices included.

### 🎯 SEO Optimized
- Clean semantic HTML5 structure.
- Mobile-readiness improves search engine rankings.
- Meta tags for social sharing and description.

### 💰 Cost-Effective
- AWS Free Tier covers most portfolios: 1000 build minutes, 5GB storage, 15GB transfer/month.
- Typical cost: $0-5/month after first year.
- No hidden fees or surprise charges.

### 🚀 Scalable Infrastructure
- Handles 10 or 10,000 visitors with zero configuration changes.
- Auto-scaling with CloudFront and S3.
- Pay only for what you actually use.

### 🛠️ Low Maintenance
- No servers to patch, update, or manage.
- Automatic SSL certificate renewal.
- Simple GitHub-based deployment workflow.

### 🌍 Global Reach
- Served from 450+ AWS edge locations worldwide.
- Ensures fast delivery regardless of visitor location.

---

## 📄 Amplify Build Configuration

For static HTML/CSS/JS portfolios, Amplify uses this configuration:

```yaml
version: 1
frontend:
  phases:
    build:
      commands:
        - echo "Building static portfolio site"
  artifacts:
    baseDirectory: /
    files:
      - '**/*'
  cache:
    paths: []
```

**Key Points:**
- `baseDirectory: /` - Looks for files in the root directory
- `files: - '**/*'` - Includes all files and folders
- No build commands needed for pure HTML/CSS/JS

**If your project has a build folder:**
```yaml
baseDirectory: build  # or 'dist' or 'public'
```


## 📊 Cost Breakdown

| Item | Free Tier | After Free Tier |
|------|-----------|-----------------|
| Build Minutes | 1,000/month | $0.01/min |
| Storage | 5 GB/month | $0.023/GB |
| Data Transfer | 15 GB/month | $0.15/GB |
| CloudFront CDN | Included | Included |
| SSL Certificate | Free (forever) | Free (forever) |
| Custom Domain | N/A | $8-15/year |

**Typical Portfolio (200 visitors/day):** $1.80/month  
**High-Traffic Portfolio (500 visitors/day):** $20/month

---

## 🧠 What You'll Learn

By building and deploying this portfolio, you gain hands-on experience with:

- ✅ **CI/CD Pipelines:** Automated testing and deployment workflows
- ✅ **Cloud Infrastructure:** AWS services (Amplify, S3, CloudFront, Route 53)
- ✅ **DevOps Practices:** Infrastructure as Code, automated deployments
- ✅ **DNS & SSL/TLS:** Domain management and HTTPS security
- ✅ **Git & GitHub:** Version control workflows and collaboration
- ✅ **Performance Optimization:** CDN, caching, and global delivery
- ✅ **Monitoring & Logging:** CloudWatch metrics and error tracking

These are **in-demand skills** for DevOps and Cloud Engineering roles!

---

## 🕵️ Troubleshooting

### Problem: Build succeeds but site shows "Welcome" page

**Solution:**
- Ensure `index.html` is in the **root directory**
- Update build settings: `baseDirectory: /`
- Redeploy the app

### Problem: Changes not appearing after git push

**Solution:**
- Hard refresh browser: `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
- Check Amplify Console to confirm build completed
- Wait 2-3 minutes for deployment to finish

### Problem: Custom domain SSL stuck at "Pending"

**Solution:**
- Verify DNS records in your domain provider match Amplify's CNAME records exactly
- Wait 15-30 minutes for DNS propagation
- If still stuck, delete the domain and re-add it

---

### screenshost
**amplify dashboard**
<img width="1917" height="959" alt="amplify" src="https://github.com/user-attachments/assets/17ad9afb-92a2-47d7-9f70-ce1fd5231af8" />
**logs**
<img width="1919" height="955" alt="log" src="https://github.com/user-attachments/assets/e23a1a58-757b-404b-8a5d-5c3ef17aa615" />
**metric**
<img width="1919" height="1003" alt="metric" src="https://github.com/user-attachments/assets/0a8d305d-e659-489c-986e-310868397ab7" />
**domain - route-53**
<img width="1919" height="1079" alt="domain" src="https://github.com/user-attachments/assets/03906d1e-2877-4719-8e8e-36d272b7e1ed" />

## 👤 About This Project

**Built by:** Santhosh Raj V
**Purpose:** Showcase cloud/DevOps skills and deployment expertise  
**Updated:** November 2025

### Connect With Me
- **LinkedIn:** https://www.linkedin.com/in/santhoshrajv9114/
- **GitHub:** https://github.com/vsanthoshraj
- **Email:** sksanthosh88409@email.com
- **call:** 9566066846


---

## 📜 License

This project is open source and available free


---

*Last Updated: November 13, 2025*  
thank you
