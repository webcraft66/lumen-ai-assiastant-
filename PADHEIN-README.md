# LUMEN — Voice Assistant

## 📱 Mobile ka sach

- **iPhone (iOS)** — kabhi kaam nahi karega, kisi bhi browser mein. Apple ne
  voice recognition feature hi block kiya hua hai iOS mein. Isका koi solution
  nahi hai jab tak Apple khud ye policy nahi badalta.
- **Android** — kaam kar sakta hai, lekin sirf tab jab file `https://` link se
  khuli ho (jaise Vercel wala live link), local file se nahi. Neeche Vercel
  wala step follow karein.

## 💻 Laptop par chalane ka sahi tareeka (RECOMMENDED)

Laptop par ye sabse achhi tarah chalega. Do tareeke hain:

### Tareeka 1: Seedha double-click (sabse aasan, lekin limited)

`voice_assistant.html` par double-click karke Chrome mein kholein.

⚠️ **Dhyan dein:** Is tareeke se **mic kaam nahi karega**, kyunki Chrome
`file://` (local file) par microphone access allow nahi karta — ye security
ka rule hai, humara code ka bug nahi. Sirf tab UI dekhne ke liye theek hai.

### Tareeka 2: Local server se kholein (mic ke liye ZAROORI)

Mic kaam karne ke liye file ko `http://localhost` se serve karna hoga.

**Agar Python installed hai (Mac par by default hota hai):**

1. Is folder ko kisi jagah rakhein (jaise Desktop par `lumen` naam ka folder)
2. Terminal / Command Prompt kholein aur is folder mein jaayein:
   ```
   cd Desktop/lumen
   ```
3. Ye command chalayein:
   ```
   python -m http.server 8000
   ```
   (Agar ye kaam na kare, `python3 -m http.server 8000` try karein)
4. Chrome mein jaakar type karein:
   ```
   http://localhost:8000/voice_assistant.html
   ```
5. Ab mic button dabayein — permission popup aayega, "Allow" karein.

**Agar Python nahi hai (Windows par common hai):**

- **VS Code** install karein (free) → **"Live Server"** extension add karein →
  file par right-click → "Open with Live Server". Ye automatically
  `http://127.0.0.1:...` par khol dega.
- YA phir neeche wala Vercel tareeka use karein — usmein local server ki
  zaroorat hi nahi.

## 🌐 Sabse aasan tareeka: Vercel par free host kar dein

Isse laptop AUR Android mobile, dono par bina kisi local-server jhanjhat ke
kaam karega, kyunki ye seedha `https://` link banega.

1. https://vercel.com par free account banayein
2. https://vercel.com/drop par jaayein
3. `voice_assistant.html` ko is page par drag-drop karein
4. Project ka naam daalein, "Deploy" dabayein
5. Kuch second mein ek live link milega (jaise `your-name.vercel.app`) —
   ye link laptop aur Android dono mein Chrome se kholein

## 🔑 API Key

App ke andar neeche ek box hai jahan apni **free Gemini API key** paste
karni hai. Key yahan se milegi (Google account se, bilkul free):

https://aistudio.google.com/app/apikey

Key ko "Save key" button se save karein, phir mic dabakar baat shuru karein.

## ✅ Quick checklist agar kaam na kare

- [ ] Chrome ya Edge use kar rahe hain? (Safari/Firefox mein kaam nahi karega)
- [ ] URL `http://localhost...` ya `https://...vercel.app` se shuru ho raha
      hai? (`file://` se shuru ho raha ho toh mic kabhi kaam nahi karega)
- [ ] Mic permission "Allow" ki hai? (Chrome address bar ke lock icon se
      check karein)
- [ ] Gemini API key save ki hai?
- [ ] iPhone toh nahi use kar rahe? (Us par kabhi kaam nahi karega)
