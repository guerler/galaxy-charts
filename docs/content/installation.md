# Getting Started

Follow these steps to start developing a new visualization for Galaxy using the standard Vue-based setup — or explore the [Vite-only, JS-agnostic alternative](/content/xml-framework.html#building-a-vite-plugin-vanilla-vue-react-and-more) if your visualization doesn't require the built-in Vue input form.

## 1. Set Up Your Repository

1. Sign in to your [GitHub](https://github.com) account.
2. Go to the [Galaxy Charts Starter](https://github.com/guerler/galaxy-charts-starter) repository.
3. Click on **Use this template** and select **Create a new repository**.
4. Name your new repository (e.g., `MY_VISUALIZATION`), then complete the setup by clicking **Create repository**.

## 2. Clone Your Repository

Open a terminal window and clone your newly created repository:

```bash
git clone https://github.com/USERNAME/MY_VISUALIZATION
```
Replace USERNAME with your GitHub username and MY_VISUALIZATION with your repository name.

## 3. Initialize Your Visualization Project

Navigate to your project directory and set up the environment:
```bash
cd MY_VISUALIZATION
npm install
npm run dev
```

## 4. Next Steps

Open a web browser and navigate to the localhost URL displayed in your terminal (typically in the format `http://localhost:PORT`):

<div class="flex justify-around items-center p-1">
  <img class="border-2 rounded border-gray-100" src="/galaxy-charts-starter.jpg" alt="starter" width="80%">
</div>

:tada: **Congratulations!**

Your Galaxy visualization repository is set up and ready for development. Follow the instructions on the splash screen and refer to these docs as you build your custom visualization.

When you’re ready to publish, refer to the [Deploy to Galaxy](deploy-plugin.html) section to share your visualization with the Galaxy community.

Thank you for your contribution!
