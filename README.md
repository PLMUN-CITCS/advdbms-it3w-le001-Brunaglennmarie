# **2025-ADVDBMS-LE001**
Week 04 - SQL Data Definition Language

Laboratory # 01 - Guided Coding Exercise: Database Creation and Management

## **Instructions**

### **Step 1.1: Accept the Assignment**

   1. Click on the assignment link provided by your instructor.
   2. GitHub Classroom will create a **private repository** under your GitHub account.
   3. After the repository is created, click **"Go to Repository"** to view your assignment.

---

### **Step 1.2: Setup your Git Environment**
Only perform this if this is the first time you will setup your Git Environment

   1. Create a GitHub Account:
   ```bash
   https://github.com/signup?source=login
   ```
      
   2. Download and Install Git on your Laptop/Desktop:
   ```bash
   https://git-scm.com/downloads
   ```
   
   3. Create a Folder in your Laptop/Desktop
   4. Right-click anywhere in the created folder and select "Open Git Bash Here".
   5. In the Git Bash Terminal, set your git name, perform command:
   ```bash
   git config --global user.name "Your Name"
   ```
   
   6. In the Git Bash Terminal, set your git email, perform command:
   ```bash
   git config --global user.email "your.email@example.com"
   ```
   
   7. Create your SSH Key, just follow the instructions, no need to provide filename and passphrase. In the Git Bash Terminal, perform command:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   
   8. Copy your SSH Keys into clipboard. In the Git Bash Terminal, perform command:
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```
   
   9. Log in to your GitHub account.
   10. In the upper-right corner of GitHub, click your profile picture and select Settings.
   11. In the left sidebar, click on SSH and GPG keys.
   12. Click the New SSH key button.
   13. In the Title field, give the key a recognizable name (e.g., "My Windows Laptop").
   14. In the Key field, CTRL + V or paste the keys copied into your clipboard. Save the key.
   15. Go Back to terminal, use command:
   ```bash
   ssh -T git@github.com
   ```

### **Step 2: Clone the Repository to Your Local Machine**

   1. On your repository page, click the green **"Code"** button.
   2. Copy the repository URL (choose HTTPS for simplicity).
   3. Open your terminal (or Git Bash, Command Prompt, or PowerShell) and run:
   
   ```bash
   git clone <git_repo_url>
   ```
   
   4. Navigate into the cloned folder:
   
   ```bash
   cd <git_cloned_folder>
   ```

### **Step 3: Complete the Assignment**

**Laboratory # 03 - Guided Coding Exercise: Database Creation and Management**

   **Objective:**
   Learn to create, use, and drop a database using SQL. This exercise will introduce basic SQL commands and file management practices for database development.

   **Folder Structure:**
   ```txt
   university_db/
   ├── create_and_use_db.sql
   └── drop_db.sql
   ```

   **File Naming Convention:**
   - `create_and_use_db.sql`: Contains SQL statements for creating and using the database.
   - `drop_db.sql`: Contains the SQL statement for dropping the database.

   **Notable Observations (to be discussed after completing the exercise):**
   - Consistency is Key: Maintain consistent casing for database and table names to avoid potential issues.
   - Handle with Care: Dropping a database is irreversible. Use the IF EXISTS clause and double-check before executing.
   - Verification Matters: Use SELECT DATABASE(); (or equivalent) to confirm the active database.
   - Planning Ahead: This exercise is the foundation. Think about the tables needed (students, courses, etc.) before creating the database.
   - Dialect Differences: SQL syntax can vary slightly between database systems (MySQL, PostgreSQL, etc.).

   **SQL Script Best Practices**
   - Comments: Use comments (--) to explain the purpose of your SQL code. This improves readability and maintainability. Crucial for learning!
   - File Organization: Separate SQL scripts for different tasks (create, drop, etc.) promotes organization.
   - IF EXISTS Clause: Always use IF EXISTS when dropping databases or tables to prevent errors.
   - Explicit USE: Clearly specify USE <database_name>; to ensure you're working in the correct database.
   - Modular Design: Break down complex tasks into smaller, manageable scripts.
   - Version Control: Consider using version control (like Git) to track changes to your SQL scripts.
   - Indentation and Formatting: Use consistent indentation and formatting to make your SQL code easier to read.

   **Step-by-Step Instructions:**

   1. Setting up the Environment
      - Ensure you have a SQL database management system installed (e.g., MySQL, PostgreSQL, SQL Server). This exercise will use generic SQL syntax, but you might need to adjust slightly depending on your specific DBMS.
      - Create the `university_db` directory. Inside it, create the two SQL files as shown in the folder structure above.
      
   2. create_and_use_db.sql (Create and Use Database):
      - Open `create_and_use_db.sql` in a text editor.
      - Create the Database:
      ```SQL
      -- Step 1: Create a database called UniversityDB
      CREATE DATABASE `UniversityDB`;
      ```
      
      - Use the Database:
      ```SQL
      -- Step 2: Use the newly created database
      USE `UniversityDB`;
      
      -- Verification (Optional): 
      -- You can add a simple query to verify the database is selected.
      SELECT DATABASE(); -- This will show the currently selected database.
      
      ```
      
      - Save the `create_and_use_db.sql` file.
      
   3. `drop_db.sql` (Drop Database):
      - Open `drop_db.sql` in a text editor.
      - Drop the Database
         ```SQL
         -- Step 3: (Optional) Drop the database if needed. 
         -- Use with extreme caution!
         USE `UniversityDB`;
         
         -- The IF EXISTS clause prevents an error if the database doesn't exist.
         DROP DATABASE IF EXISTS `UniversityDB`;

         ```
      - Save the `drop_db.sql` file.

   4. Executing the SQL Scripts:
      - Open your SQL client (e.g., MySQL Workbench, pgAdmin, SQL Server Management Studio). Connect to your database server.
      - Creating and Using: Open the `create_and_use_db.sql` file in your SQL client or execute it from the command line. This will create the `UniversityDB` and switch the connection to use it.
      - Dropping: If you want to drop the database (e.g., to start over), open the `drop_db.sql` file in your SQL client or execute it. Be very careful with this command, as it will permanently delete the database and all its data.

### **Step 4: Push Changes to GitHub**
Once you've completed your changes, follow these steps to upload your work to your GitHub repository.

1. Check the status of your changes:
   Open the terminal and run:
   
   ```bash
   git status
   ```
   This command shows any modified or new files.
   
2. Stage the changes:
   Add all modified files to staging:
   
   ```bash
   git add .
   ```
   
3. Commit your changes:
   Write a meaningful commit message:
   
   ```bash
   git commit -m "Submitting ADVDBMS Week 04 - Session 01 - Exercise 01"
   ```
   
4. Push your changes to GitHub:
   Upload your changes to your remote repository:
   
   ```bash
   git push origin main
   ```
