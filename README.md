# Craft 3 CMS Notes

## Content Organization in Craft

**Sections**
- How content or data is organized in Craft

- News articles, set of docs, website pages

- 3 Section types in Craft:

  1. Channel
    - Used for a collection of related content (e.g news articles, blog posts, list of staff members, recipes, etc.).
    - Provide a way to organize serial content that can be added to over time.
  2. Structure
    - Groups together related content (similar to a Channel section), but in a hierarchy or nested fashion (e.g. `/about`, `/about/team`, `/about/offices`).
  3. Single
    - One-off entry with no sibling content that is meant to stand on its own (e.g. homepage, single internal pages, etc.).
    - Typically have unique content & layout requirements that are not shared with other entries.

- Review categories of existing content and determine how they should be represented by Sections

**Fields & Field Types**
- Fields help organize content into smaller pieces (e.g. A 'News Articles' Section might include Fields like 'Headline', 'Article Excerpt', 'Article Image', 'Article Body Copy', etc.

- Field Types define what type of content can be stored in a Field (e.g. A 'Headline' Field would have a Field Type of 'Title Field', 'Article Excerpt' would be a 'Plain Text Field', etc. (Craft comes with multiple Field Types)

**Matrix Fields**

- Matrix fields are the powerhouse of Craft. They allow for the creation of multiple blocks of content within a single field

- Each block can contain multiple fields and field types, and there can be multiple instances of the same block

- Matrix blocks can be re-ordered to customize layouts and content flow

- Matrix fields have two main settings:

  1. Configuration - Define which block types are available to a given Matrix field, and which sub-fields those block types should have
  2. Max Blocks - The maximum number of blocks that can be created within the Matrix field (unlimited by default)

**Entries & Templates**
- Each piece of content in Craft is stored as an Entry (e.g. a single news article in a 'News' Section, a blog post, an employee bio, etc.)

- Entries can be displayed as a Listing (set of Entries with links to each single Entry) or a Single Entry (the full Entry at a unique URL)

- Templates output content and HTML (via [Twig](https://docs.craftcms.com/v3/dev/twig-primer.html#app))

- Templates are stored inside the `/templates` directory, and can be organized in sub-directories as necessary

**Assets**
- Manage files in Craft using Assets manager

- Only stores references to files on disk

- Allows for easy access to files in control panel and in templates

- Two ways to manage asset files in Craft 3:
  1. Local - Stored right on disk of server
  2. Remote - Stored in 3rd party cloud service (AWS S3, Google Cloud, Rackspace Cloud)

- Files are stored and organized in Asset Volumes, which are created under `Settings > Assets > Volumes`
