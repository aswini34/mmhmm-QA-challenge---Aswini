# mmhmm-QA-challenge---Aswini

**List of identified bugs:**

**Main functional bugs:**

1.	Image is not rendering properly in the index page after submitting new book form.

     **Analysis:** Image is getting rendered to the whole index page. Unable to do add another new book after this issue because the book cover image is not properly rendered.
     
     **Cause:** Position of the image is not defined properly.

2.	Image is not loading properly.

     **Cause:** Image URL is not being passed properly in HTML. When I inspected the image element, the link which I entered in the form doesn’t entirely match with the src   content that is being passed.

3.	Even if the user doesn’t give the image URL while adding a new book, by default an image is rendered in the index page.

     **Cause:** By default, in HTML file some image URL is seen in the src content when the user doesn’t provide any image URL. (But sometimes that might also be a functionality in case the user doesn’t give any URL input, the code is written to take an alternate URL).

4.	Sometimes new book is not getting added in the index page.

    **Analysis:** Caught this a few times when tried to add 2 new books in one go. 

    **Cause:** In API response, the newly added book details doesn’t get fetched. So, in this case the new book is not even stored in the database.

5.	When the user simply presses enter in the “Add new” form, a new book space is getting added in the database. Even if the cursor is not on the “Add Book” button.

    **Cause:** I assume code issue here

**Other non-critical bugs/UI related issues:**

6.	Books are not getting added in the order they were entered by the user.

    **Cause:** When the user enters multiple books, they are getting added in the database in a random order because even in the API response, the order of the books that was fetched matches with the order in index page.

7.	In the “Add New” form, description field should be a text area as per the design instead of field.

    **Cause:** In the html code, the input type is given as text instead of text area.

8.	In the “Add New” form as per the design the button, to submit a new book, label should be “Save” instead of “Add Book”.

    **Cause:** In the html code, the value is displayed “Add Book”

9.	“Add Book” button CSS border is different when compared to the button given in design. 
 
    **Cause:** Border style has been added to the button


10.	When the user either provides input in any 1 or 2 of the fields, or even if the user doesn’t provide any input at in all 4 fields, still the form is getting added in the index page with or without any fields.

    **Possible solution:** We can make at least a few fields as required (mandatory fields), so that an empty book or a book with insufficient details doesn’t get added in the index page.

11.	Close button alignment is not proper.

    **Cause:** The position of the close button is not defined properly.

12.	Close button doesn’t close the form.

    **Cause:** I assume that close functionality is not defined for the button yet.

13.	Field names in the form to add a new book are not bold as given in the design document.

    **Cause:** Font styling issue

14.	Delete button icon is different in the prototype when compared with the design.

    **Cause:** Different image might have been selected in the code.

15.	Delete button functionality is not working.

    **Cause:** I assume that delete functionality is not defined for the button yet.
It would have been very useful if the button had functionality in the prototype, so that you can always delete the entries in the index page to start afresh without having to clear cookies especially when performing exploratory testing.

16.	Font for the description content is a bit different from the design.

    **Cause:** Font styling issue

**Good to have features/Future Improvements:**

1.	Edit option in the index page – it would have been very useful if there was an edit option to edit the added books.
2.	Page navigation after saving the form. 

    **Work-around:** Forced to change the URL manually to validate the index page.
    
    **Possible solution 1:** The form should be closing automatically once it is saved.

    **Possible solution 2:** The user can expect another button at the bottom of the form so that when it is clicked, it can take the user back to the index page where he can validate if the new book has been added or not.
In this case, the user should have 2 choices, one is to go back to index page after adding the number of books he intended to or second option is to stay back in the form to add another new book.

**Other finding:**
1.	Not working in IE and Firefox








