# Sentiment Analysis

This project includes a static web app that can be deployed to Netlify. It uses
a pretrained DistilBERT sentiment model in the browser and does not require a
server, Netlify Function, or API key. The Jupyter notebook remains available
for the separate model-training workflow.

## Run locally

```sh
npm install
npm run dev
```

The browser downloads the model from Hugging Face the first time an analysis is
run. The text is processed locally in the browser; it is not sent to Hugging
Face or Netlify.

## Deploy to Netlify

Connect this project directory to Netlify. Netlify reads `netlify.toml` and
uses:

- Build command: `npm run build`
- Publish directory: `dist`

Or build locally with `npm install` and `npm run build`, then deploy the
generated `dist` directory. The hosted app needs an internet connection to
download the model on the first analysis.
