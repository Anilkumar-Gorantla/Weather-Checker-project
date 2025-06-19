1.Initialize Git Repository:-
   mkdir weather-checker
   cd weather-checker
   git init
2. Create .gitignore
  echo -e "__pycache__/\n*.pyc\n.env\n.envrc\n.vscode/\n*.log" > .gitignore
  git add .gitignore
  git commit -m "Add .gitignore to exclude temporary and environment-specific files"
3.Create README
 echo "# Weather Checker\n\nA simple CLI app to check current weather using an API." > README.md
 git add README.md
 git commit -m "Add initial README with project overview"
 4. Set Up Basic Project Structure
mkdir src
touch src/main.py
echo -e "def main():\n    print('Weather Checker')" > src/main.py
git add src/
git commit -m "Create initial project structure with main script"
5. Add Functionality (Example)
# src/main.py
import requests

def main():
    city = input("Enter city name: ")
    print(f"Checking weather for {city}...")
    # Dummy print until API is added
    print("Sunny, 25°C")
git add src/main.py
git commit -m "Add basic user input and mock weather response"
6. Add Requirements File
echo "requests" > requirements.txt
git add requirements.txt
git commit -m "Add requirements.txt with requests dependency"
7. Connect to Remote Repo (Optional)
git remote add origin git@github.com:yourusername/weather-checker.git
git branch -M main
git push -u origin main

git commit -m "Fix API error when city is not found" -m "Handled 404 response by checking status code"
