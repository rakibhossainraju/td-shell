## Context

The current `settings-page.html` provides a foundation for settings with a sidebar and content area. However, it lacks "Workspace Administration" features and dynamic navigation. This design focuses on integrating Business Hours and Holiday List management into the existing structure while updating the visual theme to use `#2563eb` as the primary accent.

## Goals / Non-Goals

**Goals:**
- Add a "Workspace Administration" section to the sidebar.
- Implement "Business Hours" and "Holiday List" as sub-routes.
- Use simple client-side logic to switch between views.
- Implement the "Business Hours" configuration UI with all required parameters (Toggle, Inboxes, Timezone, Schedule, Holidays).
- Implement the "Holiday List" management UI.
- Ensure the primary accent color is `#2563eb` throughout.

**Non-Goals:**
- Backend API integration.
- Permanent data persistence.
- Refactoring the entire CSS architecture (staying within the existing single-file approach).

## Decisions

### 1. View Management (Routing)
We will use a simple JavaScript-based approach to toggle the visibility of content sections. Each settings "page" will be a `div` inside `.content-body`. Clicking a sidebar link will:
- Update the `active` class on the sidebar links.
- Hide all content sections and show the one corresponding to the clicked link.

### 2. Primary Color Theme
The CSS variables in `:root` will be used to ensure consistency. Specifically, `--color-accent` will be set to `#2563eb`. All interactive elements (toggles, primary buttons, active states) will reference this variable.

### 3. Component Structure
- **Toggles**: Custom CSS checkboxes styled as switches.
- **Selects/Inputs**: Standardized form controls following the existing design's aesthetics (DM Sans font, specific border colors).
- **Business Hours Grid**: A simple grid or list for Monday-Sunday hours.

### 4. Default Route
Upon loading, the "Business Hours" route will be selected by default as requested.

## Risks / Trade-offs

- **[Risk]** Single-file size: Adding multiple pages to one HTML file can make it large.
- **[Mitigation]** Keep the HTML semantic and the CSS concise. Use reusable utility classes where appropriate.
- **[Risk]** Complexity of "Custom Business Hours" UI.
- **[Mitigation]** Start with a simple list of days with start/end time inputs, which provides the necessary functionality without over-engineering.
