

# GitHub

# Git Commands Cheat Sheet


## Initializing a Repository
```bash
git init
```  
Is command se aap current directory ko Git repository bana sakte hain.

## Cloning a Repository

- `git clone <repository_url>`  
  Is command se aap kisi remote repository ko apne machine par clone karte hain. Yeh command aapko repository ki complete copy provide karti hai.  
  **Example:**  
  ```bash
  git clone https://github.com/Codewith-Vedant/Key-Logger
  ```

## Setting Up Remote Repository
```bash
git remote -v
```  
Is command se aap apne remote repositories dekh sakte hain.

- `git remote add origin <link>`  
  Is command se aap apne local repository ko ek remote repository (origin) se connect karte hain.

## Branching

```bash
git branch -M main
```  
Is command se aap current branch ko "main" naam se rename karte hain.

```bash
git add <filename>
```  
Is command se aap specific file ko staging area mein add karte hain. Agar aap sab files ko add karna chahte hain, toh `git add .` use kar sakte hain.

```bash
git push -u origin main
```  
`-u` flag se aap upstream branch set karte hain, jo future pushes ke liye default branch ban jata hai. Iske baad, next time se aap direct `git push` command use kar sakte hain bina `origin main` likhe.

## Checking and Managing Branches

- `git branch`  
  Is command se aap current branches dekh sakte hain.

- `git checkout -b feature1`  
  Is command se aap nayi branch "feature1" create aur switch karte hain.

- `git branch -d feature1`  
  Is command se aap "feature1" branch ko delete karte hain. Lekin, delete karne se pehle aapko main branch par switch karna hoga:  
  ```bash
  git checkout main
  ```

- `git diff`  
  Is command se aap do branches ke beech mein differences dekh sakte hain.

- `git merge main`  
  Is command se aap main branch ke changes ko current branch mein merge karte hain.

- `git pull origin main`  
  Is command se aap remote repository se changes ko apne local repository mein laate hain. Iske baad aapko local machine par changes dekhne ko milenge.

## Undoing Changes

- `git reset <filename>`  
  Is command se aap kisi specific file ko staging area mein wapas laate hain. Agar aapne file ko `git add` kiya hai, lekin commit nahi kiya hai, toh yeh command us file ko staging se remove kar dega.  
  **Example:**  
  ```bash
  git reset myfile.txt
  ```

- `git reset`  
  Is command se aap staging area ki sabhi changes ko unstage karte hain. Yeh command sabhi staged changes ko wapas working directory mein laata hai.  
  **Example:**  
  ```bash
  git reset
  ```

- `git reset HEAD~1`  
  Is command se aap last commit ko undo karte hain, lekin aapki changes working directory mein rahengi. Yeh command useful hai jab aap last commit mein kuch changes karna chahte hain.  
  **Example:**  
  ```bash
  git reset HEAD~1
  ```

## Checking Commit History

- `git log`  
  Is command se aap commit history dekh sakte hain. Yeh aapko sabhi commits ki list dikhata hai, jisme commit hash, author, date, aur commit message shaamil hote hain.  
  **Example:**  
  ```bash
  git log
  ```

## Resetting to Specific Commits

- `git reset <hash_value>`  
  Is command se aap repository ko kisi specific commit tak reset karte hain. Yeh command working directory aur staging area ko us commit ke state par le jaata hai.  
  **Example:**  
  ```bash
  git reset 1a2b3c4
  ```

- `git reset --hard <hash_value>`  
  Is command se aap repository ko kisi specific commit tak reset karte hain aur saari changes (staged aur working directory) hata dete hain. Yeh command bahut powerful hai, lekin dhyan se use karna chahiye kyunki yeh irreversible changes karta hai.  
  **Example:**  
  ```bash
  git reset --hard 1a2b3c4
  ```
