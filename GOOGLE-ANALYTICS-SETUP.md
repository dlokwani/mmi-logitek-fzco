# Google Analytics & Search Console Setup Guide
## MMI Logitek Website

---

## 📊 **Step 1: Google Analytics 4 (GA4) Setup**

### **1.1 Create Google Analytics Account**
1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account (use company email: darshan@millenium.co.in)
3. Click **"Start measuring"**
4. Enter Account Details:
   - **Account Name:** MMI Logitek
   - Check all data sharing settings (recommended)
   - Click **"Next"**

### **1.2 Create Property**
1. **Property Name:** MMI Logitek Website
2. **Reporting Time Zone:** UAE (GMT+4)
3. **Currency:** AED (UAE Dirham)
4. Click **"Next"**

### **1.3 Business Information**
1. **Industry Category:** Transportation and Logistics
2. **Business Size:** Small (1-10 employees) or Medium (11-100)
3. **Business Objectives:** Select all that apply:
   - Generate leads
   - Examine user behavior
   - Get baseline reports
4. Click **"Create"**
5. Accept Terms of Service

### **1.4 Set Up Data Stream**
1. Select **"Web"** platform
2. **Website URL:** `https://dlokwani.github.io/mmi-logitek-fzco/`
3. **Stream Name:** MMI Logitek Main Site
4. Click **"Create stream"**

### **1.5 Get Tracking Code**
1. Copy the **Measurement ID** (format: G-XXXXXXXXXX)
2. Copy the **Google tag (gtag.js)** code snippet
3. You'll need to add this to ALL pages in the `<head>` section

---

## 🔍 **Step 2: Google Search Console Setup**

### **2.1 Add Property**
1. Go to [Google Search Console](https://search.google.com/search-console/)
2. Sign in with the same Google account
3. Click **"Add Property"**
4. Select **"URL prefix"** method
5. Enter: `https://dlokwani.github.io/mmi-logitek-fzco/`
6. Click **"Continue"**

### **2.2 Verify Ownership**
**Method 1: HTML File Upload (Recommended for GitHub Pages)**
1. Download the verification HTML file
2. Upload it to your GitHub repository root
3. Commit and push to GitHub
4. Wait 1-2 minutes for GitHub Pages to deploy
5. Click **"Verify"** in Search Console

**Method 2: HTML Tag (Alternative)**
1. Copy the meta tag provided
2. Add it to the `<head>` section of index.html
3. Commit and push to GitHub
4. Click **"Verify"**

### **2.3 Submit Sitemap**
1. After verification, go to **"Sitemaps"** in left menu
2. Enter: `sitemap.xml`
3. Click **"Submit"**
4. Status should show "Success" within 24 hours

---

## 📝 **Step 3: Add Google Analytics to Website**

### **3.1 Google Analytics Code Template**
Add this code to the `<head>` section of **ALL HTML pages** (replace G-XXXXXXXXXX with your actual Measurement ID):

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### **3.2 Pages to Update**
Add the tracking code to these files (right after `<head>` tag):
- ✅ index.html
- ✅ nvocc.html
- ✅ freight-forwarding.html
- ✅ container-trading.html
- ✅ customs-clearance.html
- ✅ transportation.html
- ✅ container-domestication.html
- ✅ vessel-operating.html
- ✅ indian-spices-pulses.html

### **3.3 Enhanced Tracking (Optional)**
Add event tracking for important actions:

```html
<!-- Track Contact Button Clicks -->
<script>
  document.querySelectorAll('a[href^="mailto:"]').forEach(function(link) {
    link.addEventListener('click', function() {
      gtag('event', 'contact', {
        'event_category': 'engagement',
        'event_label': 'email_click'
      });
    });
  });
  
  document.querySelectorAll('a[href^="tel:"]').forEach(function(link) {
    link.addEventListener('click', function() {
      gtag('event', 'contact', {
        'event_category': 'engagement',
        'event_label': 'phone_click'
      });
    });
  });
</script>
```

---

## 🎯 **Step 4: Configure Goals & Conversions**

### **4.1 Key Events to Track**
In Google Analytics 4, set up these conversions:
1. **Email Clicks** - When users click darshan@millenium.co.in
2. **Phone Calls** - When users click +971 58 588 1060
3. **WhatsApp Clicks** - When users click WhatsApp link
4. **Service Page Views** - Track which services get most interest
5. **Form Submissions** (when you add contact forms)

### **4.2 Create Custom Events**
1. Go to **Admin** → **Events** → **Create Event**
2. Create events for:
   - `contact_email`
   - `contact_phone`
   - `contact_whatsapp`
   - `service_view`

---

## 📈 **Step 5: Monitor & Optimize**

### **5.1 Key Metrics to Watch**
- **Users:** Total visitors to your site
- **Sessions:** Number of visits
- **Bounce Rate:** % of single-page visits
- **Average Session Duration:** Time spent on site
- **Top Pages:** Most visited pages
- **Traffic Sources:** Where visitors come from
- **Geographic Location:** Which countries visit most

### **5.2 Weekly Checklist**
- [ ] Check total visitors and trends
- [ ] Review top landing pages
- [ ] Analyze traffic sources (organic, direct, referral)
- [ ] Check which services get most views
- [ ] Monitor bounce rate (aim for <60%)
- [ ] Review geographic data (UK, US, India, Singapore, etc.)

### **5.3 Monthly Tasks**
- [ ] Review Search Console performance
- [ ] Check for crawl errors
- [ ] Analyze search queries bringing traffic
- [ ] Review sitemap status
- [ ] Check mobile usability issues
- [ ] Monitor Core Web Vitals

---

## 🚀 **Step 6: SEO Submission Checklist**

### **6.1 Submit to Search Engines**
- [ ] Google Search Console (sitemap submitted)
- [ ] Bing Webmaster Tools - [Submit here](https://www.bing.com/webmasters/)
- [ ] Yandex Webmaster - [Submit here](https://webmaster.yandex.com/)

### **6.2 Business Listings**
- [ ] Google My Business (if you have physical office)
- [ ] Bing Places for Business
- [ ] LinkedIn Company Page
- [ ] Facebook Business Page

### **6.3 Industry Directories**
- [ ] BIFA (British International Freight Association)
- [ ] NCBFAA (National Customs Brokers & Forwarders Association)
- [ ] FFFAI (Federation of Freight Forwarders' Associations in India)
- [ ] SLA (Singapore Logistics Association)
- [ ] FMFF (Federation of Malaysian Freight Forwarders)

---

## 📞 **Need Help?**

If you need assistance with:
- Setting up Google Analytics
- Verifying Search Console
- Adding tracking codes to pages
- Interpreting analytics data

Just let me know and I can help implement these changes!

---

## 📊 **Expected Results Timeline**

- **Week 1-2:** Analytics setup, initial data collection
- **Week 3-4:** First insights on traffic sources and user behavior
- **Month 2-3:** Search Console data shows search queries and rankings
- **Month 3-6:** Organic traffic growth from SEO efforts
- **Month 6+:** Significant increase in qualified leads

---

**Last Updated:** January 3, 2026  
**Website:** https://dlokwani.github.io/mmi-logitek-fzco/  
**Contact:** darshan@millenium.co.in
