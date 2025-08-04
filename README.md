# 📚 QuizBuilder AI

AI-powered Ruby on Rails application that converts PDFs into quizzes and flashcards using OpenRouter.

---

## 🚀 Quick Setup (Single Copy-Paste)

```bash
# Clone the repository
git clone https://github.com/your-username/quizbuilder-ai.git
cd quizbuilder-ai

# Install dependencies
bundle install

# Configure database
rails db:create db:migrate

# Add required gems (if not already in Gemfile)
echo "gem 'pdf-reader'" >> Gemfile
echo "gem 'httparty'" >> Gemfile
echo "gem 'dotenv-rails'" >> Gemfile
bundle install

# Create .env file for OpenRouter API Key
echo "OPENROUTER_API_KEY=your_openrouter_api_key" > .env
echo ".env" >> .gitignore

# Setup Active Storage for file uploads
rails active_storage:install
rails db:migrate

# Generate models
rails g model Quiz title:string content:text
rails g model Flashcard question:string answer:text quiz:references
rails db:migrate

# Generate controller
rails g controller Quizzes new create show

# Start Rails server
rails server

#Upload a PDF → AI generates quizzes & flashcards → View flashcards.

# Tech Stack
Ruby on Rails 7

PostgreSQL

OpenRouter AI

pdf-reader gem

Bootstrap 5

Active Storage

#🔮 Future Improvements
Interactive flashcard flipping

Regenerate flashcards option

Multiple AI model support

Export quizzes to CSV or Anki format

User authentication for personalized storage

Dark mode and improved UI
