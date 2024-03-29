# AI Solutions Toolkit at the CSA

## Foundation Models
* Anthropic Claude
* Google Gemini
* OpenAI ChatGPT

## Prompt Engineering
* PromptPerfect.jina.ai

## Creating System Prompts
* PrmptPerfect
* CustomGPT.ai system prompt generator
* OpenAI My GPTs

## RAG Bots
* OpenAI My GPTs
* CustomGPT.ai

## Vendor specific AI

We are generally not using these at this time (e.g. Google/Office365/Zendesk/etc.)

* GitHub CoPilot (Dev team)

## Using APIs for bulk queries/work
* Anthropic Claude
* Google Gemini
* OpenAI ChatGPT
* CustomGPT.ai
* PromptPerfect

## Automation
* Zapier + AI
* OpenAI My GPTs with actions

## Training on tools, processes, workflows, techniques, etc.
* Training decks, RAG Bots as tutors/mentors

## Getting text information for the AI
* Manual downloads, SingleFile, etc.
* TODO: google chrome headless to PDF downloader/DOM Downloader service in a VM 
* Various custom scripts to convert HTML/PDF/etc. into Markdown

# Building solutions overview

Decide what to build, build it, log it in https://docs.google.com/spreadsheets/d/1-tOBliwR62TGcuh69tBQ7Rt8tF3YUm3BRHbjSnc9Gpg and ensuire the data is backed up for from a source that is backed up.

# Information on specific technologies:

TODO

## OpenAI My GPTs

**Capabilities:** These are RAG bots based on ChatGPT 4, the file ingest is limited: 20 files, each file can be up to 512 MB in size and can contain 2,000,000 tokens. No OCR, no abilitry to parse text columns e.g. do not upload a slide deck. Stick to plain text or markdown formatted text.

**Access requirements:** You must have a paid ChatGPT account to access a My GPTs bot

**Cost for the CSA to run:** none at this time

**Limitations:** There is no integration with Zapier for automated uploads of new or updated knowledge files

**Benefits:** Very quick and easy to build, costs the CSA nothing to run at this time

**Maintenance and Operational requirements:**  Very low, update the knowledge files as needed and update the instructions (system prompt) as needed.

**Resources:**

* https://help.openai.com/en/articles/8554397-creating-a-gpt
* https://help.openai.com/en/articles/8673914-gpts-vs-assistants
* https://help.openai.com/en/articles/8843948-knowledge-in-gpts
* https://help.openai.com/en/articles/8554407-gpts-faq
* https://help.openai.com/en/articles/8798878-building-and-publishing-a-gpt

### Building instructions

TODO

### Backup instructions

Backup the knowledge files and the name, description, and instructions (system prompt) to a text file in markdown format. 
