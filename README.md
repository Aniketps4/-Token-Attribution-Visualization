Token Attribution Visualization Tool
This repository contains a Jupyter notebook (Token_visualization.ipynb) that implements
an interactive tool for visualizing token-level importance in Large Language Model (LLM) 
predictions. The tool uses Gradio for the interface and supports multiple pre-trained LLMs
from Hugging Face, with enhanced visualization features.

Setup Instructions
Prerequisites
Google Colab: The notebook is designed to run in Google Colab for ease of use and resource availability.
Python 3: Ensure a compatible Python environment (Colab provides this by default).
Installation
Open in Colab:
Click the "Open in Colab" badge or upload Token_visualization.ipynb to Google Colab (https://colab.research.google.com/).
Install Dependencies:
Run the first cell in the notebook to install required libraries:

!pip install gradio transformers torch

This installs Gradio (for the interface), Transformers (for LLM integration), and PyTorch (for computation).
Run the Notebook:
Execute all cells sequentially. The Gradio interface will launch automatically, providing a public URL for interaction.
Dependencies
gradio (version 5.31.0 or later)
transformers (version 4.52.4 or later)
torch (version 2.6.0+cu124 or later, with CUDA support for Colab)
numpy (included with Colab)
Usage

How to Use the Tool
Launch the Interface:
After running the notebook, a public URL (e.g., https://*.gradio.live) will be generated. Click the link or the embedded iframe in Colab to access the tool.

Input Text:
Enter text in the "Enter text here..." textbox (e.g., "This is a great movie!").

Select Model:
Use the "Select Model" dropdown to choose from available LLMs: distilbert-base-uncased, bert-base-uncased, or roberta-base. The default is distilbert-base-uncased for its lightweight nature.

Adjust Visualization:
Use the "Emphasis on Attention Scores" slider (range: 0.5 to 2.0) to modify the color intensity of token highlights. A higher value emphasizes differences in importance.
Interact with Visualization:
The "Token Attribution Visualization" section displays tokens with colored overlays (green gradient indicates importance).
Hover over tokens to see details: token text, position, raw score, and emphasized score.

View Outputs:
Check the "Model Prediction" for the sentiment label (Positive/Negative) and probability scores.
The "Status" field confirms the visualization generation and provides usage hints.
Example Workflow
Input: "This is a great movie!"
Model: distilbert-base-uncased
Output: Tokens highlighted, prediction "Positive" (e.g., Positive: 0.549, Negative: 0.451), with "great" likely showing higher attention.
