# 🚀 Groq Setup Guide - FREE Forever ATS Resume Optimizer

Complete guide to set up Groq API for your ATS Resume Optimizer.

---

## 🎯 Why Groq?

✅ **Completely FREE** - No limits, no credit card needed
✅ **10x Faster** - Instant responses
✅ **Easy Setup** - 2 minutes total
✅ **No Tracking** - Generous rate limits
✅ **Forever Free** - No paid tier needed

---

## 📋 Step-by-Step Setup

### Step 1: Get Your Free Groq API Key (2 minutes)

1. **Go to:** https://console.groq.com
2. **Click:** "Sign up" (or sign in if you have account)
3. **Enter email** and create password
4. **Verify your email** (check inbox)
5. **Go to:** "API Keys" (left sidebar)
6. **Click:** "Create API Key"
7. **Copy the key** (starts with `gsk_`)
8. **Save it somewhere safe**

**That's it!** No credit card needed, completely free.

---

### Step 2: Deploy to Streamlit Cloud (3 minutes)

#### Option A: Update Existing App (Recommended)

If you already have a Streamlit app deployed:

**Step 1: Update files on GitHub**
1. Go to your GitHub repo
2. Delete these files:
   - `app.py` (old Anthropic version)
   - `requirements.txt` (old requirements)

3. Upload new files:
   - **`app_groq.py`** (rename to `app.py`)
   - **`requirements_groq.txt`** (rename to `requirements.txt`)

4. Click "Commit changes"

**Step 2: Add API Key to Secrets**
1. Go to your Streamlit app dashboard: https://share.streamlit.io
2. Click on your app
3. Click ⚙️ **"Settings"** (top right)
4. Click **"Secrets"** tab
5. Paste:
   ```
   GROQ_API_KEY = "gsk_your-key-here"
   ```
6. Click "Save"

**Step 3: Wait for Auto-Redeploy**
- Streamlit will automatically redeploy (1-2 minutes)
- You'll see "App is updating..."

✅ **Done!** Your app is now using Groq!

---

#### Option B: Fresh Deployment (If No Existing App)

**Step 1: Create GitHub Repo**
1. Go to: https://github.com/new
2. Name: `ats-resume-optimizer-groq`
3. Click "Create repository"

**Step 2: Upload Files**
1. Click "Add file" → "Upload files"
2. Upload:
   - `app_groq.py` (rename to `app.py`)
   - `requirements_groq.txt` (rename to `requirements.txt`)
3. Click "Commit changes"

**Step 3: Deploy on Streamlit**
1. Go to: https://streamlit.io/cloud
2. Click "New app"
3. Select:
   - Repository: your-repo
   - Branch: main
   - Main file: app.py
4. Click "Deploy"

**Step 4: Add API Key**
1. Once deployed, click ⚙️ "Settings"
2. Click "Secrets"
3. Paste: `GROQ_API_KEY = "gsk_..."`
4. Click "Save"

✅ **Done!** App is live!

---

### Step 3: Test Your App (1 minute)

1. **Visit your Streamlit URL**
2. **See the API key input in sidebar?** ✅ That's good
3. **Try it:**
   - Paste your Groq API key
   - Upload example resume
   - Paste example job description
   - Click "Analyze Resume"
4. **Download the optimized resume** ✅

**It works!**

---

## 🖥️ Local Testing (Optional)

Want to test on your computer first?

```bash
# 1. Install dependencies
pip install streamlit groq python-docx

# 2. Set API key
export GROQ_API_KEY="gsk_your-key-here"

# 3. Run the app
streamlit run app_groq.py

# 4. Visit http://localhost:8501
```

---

## 📁 Files You Need

### For Streamlit Cloud:
- ✅ `app_groq.py` → rename to `app.py`
- ✅ `requirements_groq.txt` → rename to `requirements.txt`

### Files to DELETE from GitHub (if updating):
- ❌ `app.py` (old Anthropic version)
- ❌ `requirements.txt` (old)
- ❌ `app_streamlit.py` (old)
- ❌ `requirements_streamlit.txt` (old)

### Keep in GitHub (optional):
- 📄 README.md
- 📄 .gitignore
- 📋 Other docs

---

## 🔑 API Key Formats

### Groq Key Format:
```
gsk_1a2b3c4d5e6f7g8h9i0j...
```
(Starts with `gsk_`)

### Where to Use It:

**On Streamlit Cloud (SECURE):**
```
In Settings → Secrets → Add:
GROQ_API_KEY = "gsk_..."
```

**Locally (if testing):**
```bash
export GROQ_API_KEY="gsk_..."
```

**NEVER:**
- ❌ Paste directly in code
- ❌ Commit to GitHub
- ❌ Share with others

---

## ✅ Verification Checklist

Before you consider it done:

- [ ] Created Groq account (console.groq.com)
- [ ] Created API key (starts with `gsk_`)
- [ ] Uploaded `app_groq.py` (as `app.py`)
- [ ] Uploaded `requirements_groq.txt` (as `requirements.txt`)
- [ ] Added API key to Streamlit Secrets
- [ ] Streamlit app redeployed
- [ ] Can access your app URL
- [ ] Can input API key without error
- [ ] Can analyze a sample resume
- [ ] Can download optimized resume

✅ **All checked?** You're done!

---

## 🚀 Your App URL

Once deployed, your app will be at:
```
https://your-username-ats-resume-optimizer-groq.streamlit.app
```

**Share this URL with anyone!**
They can use it for free.

---

## 💡 Important Notes

### Rate Limits
- Groq offers generous free limits
- Most users won't hit them
- It's truly unlimited for normal usage

### Quality
- Groq uses Mixtral-8x7b model
- Slightly less advanced than Claude/GPT-4
- Still excellent for resume optimization
- Much faster (10x speed advantage)

### Privacy
- Data sent to Groq servers
- Not used for training
- Similar to other AI APIs

---

## 🆘 Troubleshooting

### "ModuleNotFoundError: No module named 'groq'"
**Solution:**
- Make sure you renamed `requirements_groq.txt` to `requirements.txt`
- Check file is uploaded to GitHub
- Redeploy in Streamlit settings

### "Error: Could not authenticate with Groq API"
**Solution:**
- Verify API key starts with `gsk_`
- Check key is correct (no extra spaces)
- Go to console.groq.com to verify key exists
- Verify key is in Streamlit Secrets (not sidebar input)

### "App is very slow"
**Solution:**
- This shouldn't happen with Groq (it's 10x faster!)
- Try restarting the app
- Check your internet connection
- Verify API key is valid

### "JSON parsing error"
**Solution:**
- This is rare with Groq
- Try again (sometimes it returns different format)
- Make sure resume and job description are clear
- Try with shorter inputs if very long

---

## 🔄 Switching Back to Anthropic

If you ever want to switch back:

1. Go to GitHub repo
2. Upload `app.py` (Anthropic version)
3. Upload `requirements.txt` (Anthropic version)
4. Update Streamlit Secrets to use `ANTHROPIC_API_KEY`
5. Done!

Easy to switch between APIs.

---

## 📊 Groq vs Anthropic Comparison

| Feature | Groq | Anthropic |
|---------|------|-----------|
| Cost | FREE | $5 free + paid |
| Speed | 10x faster | Normal |
| Quality | Very good | Excellent |
| Setup | Easy | Easy |
| Rate Limits | Generous | Strict |
| API Key | gsk_... | sk-ant-... |

---

## 🎓 Next Steps

### Right Now:
1. ✅ Get Groq API key (console.groq.com)
2. ✅ Upload new files to GitHub
3. ✅ Add API key to Streamlit Secrets
4. ✅ Wait 2 minutes for redeploy

### After Deploy:
1. ✅ Test your app
2. ✅ Download optimized resume
3. ✅ Share URL with friends

### Optional:
1. 📄 Create local version for offline use
2. 🔧 Customize app.py to your liking
3. 📊 Experiment with different prompts

---

## 💬 Getting Help

### Groq Issues:
- **Groq Docs:** https://console.groq.com/docs
- **Get API Key:** https://console.groq.com

### Streamlit Issues:
- **Streamlit Docs:** https://docs.streamlit.io
- **Deploy Help:** https://docs.streamlit.io/streamlit-cloud

### App Issues:
- Check FIX_STREAMLIT_ERROR.md
- Verify file names are correct
- Check requirements.txt content

---

## 📝 File Checklist

### Files to Have Ready:

```
app_groq.py
requirements_groq.txt
```

### Files to Upload to GitHub (with correct names):

```
✅ app.py (from app_groq.py)
✅ requirements.txt (from requirements_groq.txt)
```

### Files to DELETE from GitHub (if updating):

```
❌ app_streamlit.py
❌ requirements_streamlit.txt
❌ app.py (old Anthropic version)
❌ requirements.txt (old version)
```

---

## 🎉 Summary

| Step | Time | What To Do |
|------|------|-----------|
| 1 | 2 min | Get Groq API key |
| 2 | 2 min | Rename and upload files |
| 3 | 2 min | Add API key to Secrets |
| 4 | 2 min | Wait for redeploy |
| **Total** | **8 min** | **FREE, Forever!** |

---

## 🌟 Benefits of Groq Setup

✅ **Completely Free**
- No credit card
- No expiration
- Unlimited usage
- No hidden costs

✅ **10x Faster**
- Instant responses
- Great user experience
- Instant feedback

✅ **Easy to Use**
- Same interface
- Same features
- Same results
- Better speed & price

✅ **Production Ready**
- Can run 24/7
- Can handle traffic
- Scalable
- Reliable

---

## 🚀 You're Ready!

Everything you need is here.
Just follow the steps above.
You'll have a free, fast ATS Resume Optimizer in 8 minutes!

**Start with Step 1: Get your Groq API key →** https://console.groq.com

---

**Questions?** Check the troubleshooting section above.

**Ready?** Let's go! 🎉
