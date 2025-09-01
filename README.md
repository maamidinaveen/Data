In this project, I built a nested checkbox system with three levels — Select All, categories, and individual items. The goal is to keep them all synchronized.

First, I created a Select All event listener. Whenever it is checked or unchecked, it applies the same state to all category checkboxes and all individual items. This way, the user can select or deselect everything at once.

Second, I added listeners to the category checkboxes like Fruits or Vegetables. When a category is checked, all of its child items get checked automatically. If it’s unchecked, all child items are unchecked. This handles the parent-to-child relationship.

Third, I handled the individual items. If the user checks or unchecks one item, the code runs two helper functions:

updateCategory() → It verifies if all the items in a category are selected. If yes, it keeps the category checkbox checked; if not, it unchecks the category.

updateSelectAll() → It verifies if all categories are fully selected, and only then it checks the Select All box.

The logic ensures two-way synchronization:

From top to bottom, selecting higher levels (like Select All or a category) automatically updates all children.

From bottom to top, selecting or deselecting individual items updates their parent category and also the Select All state.

Overall, this gives a consistent user experience where the checkbox states always stay in sync, no matter where the user clicks.
