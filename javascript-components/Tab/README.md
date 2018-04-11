# Tab

Tabs are a set of layered sections of content, known as tab panels, that display one panel of content at a time. Each tab panel has an associated tab element, that when activated, displays the panel. The list of tab elements is arranged along one edge of the currently displayed panel, most commonly the top edge.

Terms used to describe this design pattern include:

## Tabs or Tabbed Interface
A set of tab elements and their associated tab panels.
## Tab List
A set of tab elements contained in a tablist element.
## tab
An element in the tab list that serves as a label for one of the tab panels and can be activated to display that panel.
tabpanel
The element that contains the content associated with a tab.
When a tabbed interface is initialized, one tab panel is displayed and its associated tab is styled to indicate that it is active. When the user activates one of the other tab elements, the previously displayed tab panel is hidden, the tab panel associated with the activated tab becomes visible, and the tab is considered "active".