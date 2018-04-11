# Tab

Tabs are a set of layered sections of content, known as tab panels, that display one panel of content at a time. Each tab panel has an associated tab element, that when activated, displays the panel. The list of tab elements is arranged along one edge of the currently displayed panel, most commonly the top edge.

Terms used to describe this design pattern include:

## Tabs or Tabbed Interface
A set of tab elements and their associated tab panels.
## Tab List
A set of tab elements contained in a tablist element.
## Tab
An element in the tab list that serves as a label for one of the tab panels and can be activated to display that panel.
tabpanel
The element that contains the content associated with a tab.
When a tabbed interface is initialized, one tab panel is displayed and its associated tab is styled to indicate that it is active. When the user activates one of the other tab elements, the previously displayed tab panel is hidden, the tab panel associated with the activated tab becomes visible, and the tab is considered "active".

## Keyboard Interaction
### For the tab list:

**Tab:** When focus moves into the tab list, places focus on the active tab element . When the tab list contains the focus, moves focus to the next element in the page tab sequence outside the tablist, which is typically either the first focusable element inside the tab panel or the tab panel itself.
When focus is on a tab element in a horizontal tab list:
**Left Arrow:** moves focus to the previous tab. If focus is on the first tab, moves focus to the last tab. Optionally, activates the newly focused tab (See note below).
**Right Arrow: **Moves focus to the next tab. If focus is on the last tab element, moves focus to the first tab. Optionally, activates the newly focused tab (See note below).

***When focus is on a tab in a tablist with either horizontal or vertical orientation:***

**Space or Enter:** Activates the tab if it was not activated automatically on focus.
**Home (Optional):** Moves focus to the first tab
**End (Optional):** Moves focus to the last tab.
**Shift + F10:** If the tab has an associated pop-up menu, opens the menu.
**Delete (Optional):** If deletion is allowed, deletes (closes) the current tab element and its associated tab panel. If any tabs remain, sets focus to the tab following the tab that was closed and activates the newly focused tab. Alternatively, or in addition, the delete function is available in a context menu.


##WAI-ARIA Roles, States, and Properties
- The element that serves as the container for the set of tabs has role **`tablist`**.
- Each element that serves as a tab has role **`tab`** and is contained within the element with role `tablist`.
- Each element that contains the content panel for a tab has role `tabpanel`.
- Each element with role **tab** has the property `aria-controls` referring to its **associated tabpanel element**.
- The active tab element has the state `aria-selected` set to **`true`** and all other tab elements have it set to **`false`**.
- Each element with role **tabpanel** has the property `aria-labelledby` referring to its **associated tab element**.
- If a tab element has a **pop-up menu**, it has the property **`aria-haspopup` set to either menu or `true`**.
- If the tablist element is vertically oriented, it has the property `aria-orientation` set to `vertical`. The **default value** of `aria-orientation` for a tablist element is `horizontal`.

**Special Note** - All content mentioned here has been extracted from the following link - https://www.w3.org/TR/wai-aria-practices-1.1/#tabpanel


