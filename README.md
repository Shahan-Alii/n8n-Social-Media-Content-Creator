
# Automated Social Media Content Creator

An end-to-end automation built with **n8n**, **AI**, and **Zapier** that generates, designs, and schedules social media content automatically — from idea to ready-to-post visuals.

---



<img width="1647" height="601" alt="Image" src="https://github.com/user-attachments/assets/7b135c7a-dadb-414c-bf03-4b850aa7ff59" />

<img width="597" height="433" alt="Image" src="https://github.com/user-attachments/assets/4d26aec6-41d6-46cb-b8ab-44ed7dc6b035" />


## Overview

Creating and scheduling daily social media posts can be repetitive and time-consuming.
This project demonstrates how **AI and workflow automation** can handle the entire process — ideation, caption writing, image generation, and publishing — without human intervention.

The system fetches a random fact, generates a caption and image, uploads the result, and queues it for posting via Buffer, all automatically.

---

## How It Works

1. **Fetch Random Fact:**
   n8n retrieves a random fact from a public API.

2. **Generate Caption & Image:**
   Uses **OpenRouter (Gemini)** to create an engaging caption and corresponding image prompt.
   The image is generated and uploaded to **ImgBB**.

3. **Store & Schedule:**
   The caption, image URL, and metadata are saved to **Google Sheets**.

4. **Auto-Posting:**
   A **Zapier workflow** monitors the sheet and triggers **Buffer** to schedule posts across connected social platforms.

---

## Workflow Summary

| Step               | Tool                | Purpose                                |
| ------------------ | ------------------- | -------------------------------------- |
| Random Fact Fetch  | n8n HTTP Request    | Get content ideas                      |
| AI Caption & Image | OpenRouter (Gemini) | Generate creative captions and visuals |
| Image Upload       | ImgBB               | Host generated image                   |
| Data Storage       | Google Sheets       | Save caption, image link, and metadata |
| Auto-Publish       | Zapier + Buffer     | Schedule posts automatically           |

---

## Tech Stack

* **Automation:** n8n
* **AI Generation:** OpenRouter (Gemini)
* **Storage:** Google Sheets
* **Image Hosting:** ImgBB
* **Scheduling:** Zapier + Buffer

---

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/automated-social-media-content-creator.git
   cd automated-social-media-content-creator
   ```

2. **Import Workflow**

   * Open **n8n dashboard**
   * Click **“Import from File”**
   * Upload the workflow JSON file (`SocialMediaContentCreator.json`)

3. **Connect Credentials**

   * API connection for random fact source (e.g., `uselessfacts.jsph.pl`)
   * OpenRouter (Gemini) API for caption generation
   * ImgBB API for image uploads
   * Google Sheets API for saving post data
   * Zapier + Buffer setup for automated scheduling

4. **Configure Workflow Variables**

   * Update API keys and endpoint URLs
   * Adjust caption style or image generation prompts
   * Link the correct Google Sheet and Buffer profile

5. **Activate Workflow**

   * Set workflow to “Active” in n8n
   * The system will automatically create and queue new posts

---



## Potential Use Cases

* Daily motivational or educational posts
* Automated brand updates and product highlights
* Personalized AI-generated content for clients
* Full video or short-form content creation using visual AI models like **Sora**

---

## Results

* Fully automated post creation and scheduling
* Zero manual effort for daily content generation
* Consistent posting pipeline powered by AI and automation tools

---

## Files Included

* `SocialMediaContentCreator.json` — Full n8n workflow export
* Optional Zapier/Buffer integration setup guide

---

## Future Enhancements

* Integration with **Twitter/X**, **LinkedIn**, or **Instagram APIs** for direct posting
* AI sentiment tuning for tone-adjusted captions
* Automated hashtag generation and analytics tracking

---

=

> “A fully automated n8n workflow that creates, designs, and schedules AI-generated social media posts.”
