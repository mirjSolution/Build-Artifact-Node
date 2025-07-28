# 🛠️ Build an Artifact - (JavaScript/Node.js)

After code is written, it must be **packaged** into a single file — an **artifact** — that can be easily deployed to servers for production use. This is done using **build tools**, which vary based on programming language.

---

## 📆 What is an Artifact?

An **artifact** is a packaged version of your application, including:

- Your source code
- All required dependencies (Node modules)
- Optional configuration files

### ➡️ Why Artifacts Matter:

- Easy to move between environments (dev ➡️ test ➡️ prod)
- Stored in **artifact repositories** (e.g., GitHub Packages, JFrog Artifactory)
- Ensures consistent and reliable deployments

---

## 🧰 Build Tools for JavaScript / Node.js

### **Sample Workflow for Node.js Hello World App**

![Node.js](Images/node.gif)

1. Initialize Node.js Project

```bash
mkdir hello-world-node
cd hello-world-node
npm init -y
```

2. Create `index.js` File

```javascript
// index.js
console.log("Hello World");
```

3. Package as Artifact

- Add a build script in `package.json`:

```json
"scripts": {
  "start": "node index.js",
  "build": "zip -r hello-world-node.zip index.js package.json"
}
```

4. Run Build Script

```bash
npm run build
```

- This will generate a `artifact.zip` containing your code and dependencies.

5. Run the Artifact

```bash
unzip artifact.zip
node index.js
```

- Expected Output:

```bash
Hello World
```

---

## 🧪 How It Works – Build Process Summary

1. **Install Dependencies** (via `npm install`)
2. **Package Code** into a `.zip` (or other format)
3. **Store Artifact** for deployment or sharing

---

## 📌 Final Thoughts

Understanding **build tools** and **artifact packaging** in Node.js is crucial for DevOps engineers to automate packaging, ensure deployment consistency, and manage dependencies effectively. With the right tools and artifact strategy, you streamline software delivery across any environment.

🧑‍💻 _Created by Rico John Dato-on_  
🔗 [LinkedIn](https://www.linkedin.com/in/rico-john-dato-on) • [Portfolio](https://ricodatoon.netlify.app)
