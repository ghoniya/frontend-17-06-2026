Q.1.Trace the journey of a 'View Menu' request from the browser to the server and back.
#Identify the specific role of DNS, the web server, and the HTTP response in this sequence. Then
explain why a returning customer might see the menu load faster on a second visit, and which
part of the client-server model is responsible for that behaviour

  The browser first checks whether it already knows the website's IP address.

  DNS translates the website's domain name

  Role of the web server: It receives the request, processes  and prepares the requested content.

  Role of the HTTP response: The server returns an HTTP response containing:
   
  q- 2 Identify the specific HTML form element you would use for each of the three inputs
above. For each choice, justify why that element is semantically correct for the type of data it
captures — and explain why using a plain <input type='text'> for all three would be a poor
decision.

Cash, Card and UPI use the element is <select> and <input type="radio"> and address for future order.
Addresses are often multi-line and can vary in length. <textarea> is designed for longer, multi-line text input.

why using a plain <input type='text'> for all three would be a poor decision.

beacause a text input does not indicate that the payment method should be selected from a fixed set of options.

credit card or UPI payment making the data difficult to process

<select> or radio buttons restrict input to valid choices, whereas a text field accepts any text.

A single-line text input is inconvenient for entering long or multi-line addresses.

q-3 Name the HTML5 semantic elements that should replace the generic <div> tags in
each of the four areas listed above. Then explain two specific consequences of using <div> for
everything: one related to how a screen reader would interpret the page, and one related to how
a search engine would rank it.

 HTML5 semantic element  that should replace the generic <div> tags list


 Header section- <header>-Represents  website logo, title, or navigation.

 Navigation bar-  <nav> Contains navigation links.

 Main content- <main>-website main contant

 Footer section-<footer>-copyright, contact details, or links.

 when semantic elements are used, which can improve indexing.and SEO maintain
  
  q-4 Explain the core difference in how position: absolute and position: fixed behave
relative to the page and the viewport. Identify which value is correct for the always-visible cart
panel, and list the additional CSS properties (with example values) you would need to place it in
the top-right corner without overlapping the main content.

# position relative

Moves when the page is scrolled because it is part of the document layout.

relative position used for placing elements inside a container.

# position fixed

Stays in the same place even when the page is scrolled.

Commonly used for sticky UI elements like navigation bars and buttons .

the cart panel visible at all times.
The panel remains in the same position in the browser viewport, even when the user scrolls.

q-5 Describe the Flexbox properties you would apply to the container element and to
each individual card to produce a 4-column desktop layout that reflows to 2 columns on tablet.
Then explain one specific layout scenario — for example, handling unequal card heights in a row
— where CSS Grid would give you more precise control than Flexbox.

create a responsive card layout, apply Flexbox properties to the container.

each card 25% of the container width, creating 4 columns.
On a desktop, four product cards appear in each row.

each card 50% of the container width, creating 2 columns.
On a tablet, the cards automatically wrap into two columns without changing the HTML structure.

q-6 Explain how a SASS variable solves this maintenance problem compared to editing a
plain CSS file. Additionally, describe how SASS nesting would simplify the rules for a restaurant
card component whose title, image, and 'Order Now' button currently each have their own
separate top-level CSS rule set — and why this is harder to achieve in standard CSS.

A SASS variable allows you to store a value (such as a color, font size, or spacing) in one place and reuse it throughout the stylesheet.

SASS nesting allows related CSS rules to be grouped inside the parent component instead of writing separate top-level selectors.

All styles for the restaurant card (title, image, and button) are contained within the .restaurant-card block.

Improves readability: Developers can easily see which elements belong to the card component.