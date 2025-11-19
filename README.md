# Vocabulary Constraint Experiment

An interactive web-based experiment that studies typing behavior under vocabulary constraints. Participants answer questions using only words from a limited vocabulary set.

## Features

- **Vocabulary Constraints**: Participants can only use words from a predefined vocabulary
- **Real-time Validation**: Invalid words are blocked as the user types
- **Keystroke Tracking**: Records typing efficiency and latency for each word
- **Visual Feedback**: Color-coded word analysis showing typing performance
- **Data Collection**: Automatically sends experimental data to a server

## Setup Instructions

### For GitHub Pages Deployment

1. **Create a new GitHub repository** (make it public for free GitHub Pages)

2. **Initialize and push this repository:**
   ```bash
   cd vocab-experiment-gh-pages
   git init
   git add .
   git commit -m "Initial commit: Vocabulary experiment"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under **Source**, select branch: `main` and folder: `/ (root)`
   - Click **Save**

4. **Access your site:**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`
   - It may take 1-2 minutes for the site to be available

## Configuration

### Experiment ID

The experiment ID is configured in `index.html` (line ~481):
```javascript
this.EXPERIMENT_ID = 207; // Configure this variable as needed
```

Change this value to match your experiment setup.

### Vocabulary Size

The default vocabulary size is set in `index.html` (line ~614):
```javascript
const vocabPath = 'data/word_families/vocab_250/vocabulary_250.json';
```

Available vocabulary sizes:
- `vocab_250` - 250 word families (~489 word forms)
- `vocab_500` - 500 word families (~1,065 word forms)
- `vocab_1000` - 1,000 word families (~2,189 word forms)
- `vocab_2000` - 2,000 word families (~4,208 word forms)
- `vocab_4000` - 4,000 word families (~7,563 word forms)
- `vocab_8000` - 8,000 word families (~13,519 word forms)
- `vocab_16000` - 16,000 word families (~23,947 word forms)

To change the vocabulary size, update the `vocabPath` variable to point to the desired vocabulary file.

## File Structure

```
vocab-experiment-gh-pages/
├── index.html                    # Main experiment page
├── data/
│   └── word_families/
│       ├── vocab_250/
│       │   └── vocabulary_250.json
│       ├── vocab_500/
│       │   └── vocabulary_500.json
│       └── ... (other vocab sizes)
├── README.md                     # This file
└── .gitignore                    # Git ignore file
```

## How It Works

1. **Consent Screen**: Participants enter their participant ID and consent to data collection
2. **Vocabulary Loading**: The experiment loads a vocabulary file based on the configured path
3. **Typing Constraints**: Users can only type words that exist in the vocabulary
4. **Real-time Analysis**: Each word's typing efficiency and latency are tracked
5. **Data Submission**: Results are automatically sent to the configured server endpoint

## Data Collection

The experiment collects:
- Participant ID
- Prompt responses
- Word-level typing data (keystrokes, efficiency, latency)
- Trial start and end times
- Complete word history with corrections

Data is sent to: `https://noisy-comp-server-311aa565092d.herokuapp.com/api/submit_experiment/{EXPERIMENT_ID}`

## Local Testing

To test locally before deploying:

```bash
# Using Python 3
python3 -m http.server 8000

# Then visit: http://localhost:8000/
```

## License

[Add your license information here]

## Contact

[Add contact information here]

