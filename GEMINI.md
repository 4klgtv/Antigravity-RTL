# RTL & Vazirmatn Font Rule for Persian Artifacts

When generating, editing, or displaying Markdown artifacts (such as `task.md`, `implementation_plan.md`, `walkthrough.md`, or other reports) that contain Persian text, you MUST prepend the following styling code block at the very top of the markdown file. This ensures the artifact viewer renders the content in Right-to-Left (RTL) format with the "Vazirmatn" font, while maintaining Left-to-Right (LTR) style for code and technical sections.

```html
<style>
  @import url('https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn@v33.003/Vazirmatn-font-face.css');
  
  /* Apply RTL and Vazirmatn font to text container and body elements */
  .markdown-body, p, li, h1, h2, h3, h4, h5, h6, table, tr, td, th, div, span, strong, em, a {
    font-family: 'Vazirmatn', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif !important;
    direction: rtl !important;
    text-align: right !important;
  }
  
  /* Keep code blocks, inline code, math, and keys in LTR and monospace */
  code, pre, pre *, code *, .latex, .math, math, kbd, .monospace {
    direction: ltr !important;
    text-align: left !important;
    font-family: Menlo, Monaco, Consolas, "Fira Code", "Courier New", monospace !important;
    display: inline-block;
  }

  pre code {
    display: block !important;
  }
  
  /* Adjust lists padding for RTL layout */
  ul, ol {
    padding-right: 25px !important;
    padding-left: 0 !important;
  }
  
  /* Fix blockquote borders and padding for RTL */
  blockquote {
    border-left: none !important;
    border-right: 4px solid #dfe2e5 !important;
    padding: 0 15px 0 0 !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
  }
</style>
```

Always follow this layout for Persian-containing artifacts.
