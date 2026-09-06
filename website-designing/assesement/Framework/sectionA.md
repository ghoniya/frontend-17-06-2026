<!-- s-1 Explain how Bootstrap's container, row, and col-* classes work together to create this
responsive multi-column layout. Why would applying col-12 col-md-6 col-lg-3 on each cuisine
category box produce the correct behaviour at each breakpoint -->

container: which sets a max-width at each responsive breakpoint

row: Creates a horizontal grid row and uses negative margins to properly align columns with the container.
col: Determines how much of the row’s 12-column grid each element occupies

Small/mobile screens: col-12 makes each cuisine box occupy the entire row, so they stack vertically.

Medium screens (md and above): col-md-6 overrides the 12-column width, giving each box half the row. Therefore, two boxes fit per row.

Large screens (lg and above): col-lg-3 overrides the previous width, giving each box one-quarter of the row. Therefore, four boxes fit per row.

<!-- S-2 Describe how Bootstrap's Navbar component achieves the hamburger collapse
behaviour on smaller screens. Which classes and HTML attributes make this possible, and what
would break if you removed the navbar-toggler element from the markup? -->


Bootstrap’s Navbar achieves the hamburger/collapse behaviour using a combination of responsive classes, a toggle button, and data-bs-* attributes.

# class:

# navbar:
Defines the element as a Bootstrap navbar.

# navbar-toggler:
Style the hamburger button that users click on smaller screens

# navbar-collapse:
Identifies the section containing the links as the part that should be collapsed/expanded.

<!-- s-3 How do Bootstrap's floating label pattern and validation state classes (is-valid,
is-invalid, valid-feedback, invalid-feedback) work together to guide users through form errors?
What advantage do floating labels offer over static placeholder text in a checkout flow? -->

is-valid → indicates successful validation, usually with a green visual state.

is-invalid → indicates an error, usually with a red visual state.

valid-feedback → displays a success message.

invalid-feedback → displays an error message.

<!-- s-4 Explain how Bootstrap's spacing utilities (m-*, p-*) and display utilities (d-none,
d-md-block, etc.) can accomplish all three requirements. What naming convention does
Bootstrap use for responsive display utilities, and in what order do you apply the classes? -->

m-* - margin
p-* -padding
small screens:d-none - hidden
md and large:d-md-block - displayed as a block
# example

<!-- <div class="d-none d-md-block">
    Desktop content
</div> -->

# What order should you apply the classes?

Bootstrap uses a mobile-first approach. Start with the default/mobile behaviour, then add breakpoint-specific classes for larger screens.

<!-- s-5 How would you respond to this argument? Compare Tailwind's utility-first approach
with Bootstrap's component-based approach, identifying one concrete advantage and one
concrete disadvantage of each in the context of a rapidly iterating food delivery product -->


# Bootstap
# advantages
Responsive Design: Mobile-first approach automatically adjusts layouts, text, and images for phones, tablets, and desktops

Components such as navbars, buttons, forms, modals, and responsive grids are already designed


# Disadvantages
 Writing custom CSS to override specific default component designs can get messy and complicated



# tailwind
Tailwind CSS 4 can automatically detect many project source files, reducing the need to maintain a manual content array.


<!-- s-6 Why does Bootstrap follow a mobile-first design philosophy, and how does this affect
the order in which breakpoint classes are written? Explain what would happen to the card grid
layout if you switched to a desktop-first approach using max-width media queries instead -->

Bootstrap follows a mobile-first philosophy because mobile screens have less space and force the designer to prioritize the most important content first. The layout then progressively adapts as more screen space becomes available.

A desktop-first design would start by defining the large-screen layout, then use max-width media queries to progressively change it for smaller screens.

