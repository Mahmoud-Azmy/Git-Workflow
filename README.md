# **Git Workflow for Branch Synchronization**

## **Objective**

This guide ensures a smooth workflow when multiple developers are working on different branches by keeping all branches synchronized with the latest changes in `main-branch`.

---

## **Recommended Workflow**

### **1. Merge `origin/feature-branch-1` into `main-branch`**

Since the `feature-branch-1` branch is completed and pushed, it should first be merged into `main-branch` before other branches sync their changes.

---

### **2. Each Developer Pulls the Latest `main-branch`**

Every developer working on separate branches (`feature-branch-2`, `feature-branch-3`, `feature-branch-4`, etc.) should update their branch with the latest `main-branch` changes.

#### **Steps:**

```bash
git checkout feature-branch-2        # Switch to your branch
git pull origin main-branch          # Pull the latest main branch changes
git merge main-branch                # Merge into your branch
```

> **Note:** If there are conflicts, resolve them before proceeding.

---

### **3. Continue Working and Push to Your Branch**

After merging `main-branch` into your branch and resolving any conflicts, you can continue working and push your updated branch.

#### **Steps:**

```bash
git add .                            # Stage all changes
git commit -m "Merged latest main branch updates"
git push origin feature-branch-2     # Push the updated branch
```

---

## **Summary**

1. **Merge completed branches** (like `origin/feature-branch-1`) into `main-branch` first.
2. **Each developer pulls the latest `main-branch`** into their branch to keep it up to date.
3. **Resolve conflicts**, if any, and push updates to your respective branches.

This approach ensures all branches are synchronized, reducing merge conflicts and keeping the project stable. 🚀
