# ReadMe

## Minimum Viable Product
ReadMe will be an ebook self publishing platform. Users of the site will be able to:

- [x] Create accounts
- [x] Create sessions (log in)
- [x] Upload epubs
- [x] Open epubs in an eReader
- [x] Leave reviews for books
- [x] Search books by title

## Bonus Features

- [ ] Create personal libraries
- [ ] Comment on collections
- [ ] Create collections
- [ ] Search books by subject
- [ ] Search collections by title

## Design Docs
* [View Wireframes][views]
* [DB schema][schema]

[views]: ./docs/views.md
[schema]: ./docs/schema.md

## Implementation Timeline

### Phase I: User Authentication, Upload/Download files (~2 days)

I will create a user authentication system a la that which we performed for the fourth assessment. A successful account will redirect a user to their show page, a simple rails view for now. A user's show page will contain both their library and their self published works. This page will have a form to create books. Uploaded works will have a simple show page. From this show page, users can add the book to their libraries and download the file. App in this phase should be functional and will be pushed to Heroku by the end of the second day. Primary purpose of this phase is to establish and ensure basic functionality. At this moment I do not know how to incorporate external file storage. I expect most of phase I will be spent learning how to do this.

Update:
I will combine the latter half of Phase I and II. I will be omitting the early stage file upload app. I am proceeding directly into backbone.

### Phase II: Backbone Users, Books, Libraries and Collections (~2 days)

I will add API routes to provide model data in JSON and the corresponding Backbone models, collections and routes to fetch the data. This phase will involve the construction of a functional Backbone App with which users can create accounts, log in, create books, add books to their libraries, and add books to collections.

### Phase III: Ereader (~1 day)

I will create an eReader view that will provide a user friendly reading experience for the requested file. I plan to use the Future Press javascript library to accomplish this. This functionality will be more conceptually fleshed out when I learn how to deal with managing externally stored files.

### Phase IV: Search and Subjects (~1-2 days)

I will add subjects and book-subjects models, controllers, and collections to backbone and rails. Users will be able to search for books by title, author, and subject. Users will be able to search for collections by title and description. The search page will be a composite view of a books index view and collections index view, both of which will be produced using collections of books and collections.

### Phase V: Collection Comments and Book Reviews (~1-2 days)

I will add comments and reviews models, controllers and collections to backbone and rails. Comments will allow Users to post text comments to collections that will be viewable on the collection's show page. Reviews will allow users to give a qualitative and quantitative review to a book. Review will be visible on the book's show page.
