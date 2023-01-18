class Book {
    constructor(title, author, genre, rating, notes) {
        this.title = title;
        this.author = author;
        this.genre = genre;
        this.rating = rating;
        this.notes = notes;
    }
}

class BookCollection {
    constructor() {
        this.books = [];
    }
    addBook(book) {
        this.books.push(book);
    }
    removeBook(title) {
        this.books = this.books.filter((book) => book.title !== title);
    }
    getBooks() {
        return this.books;
    }
    searchBooks(searchTerm) {
        return this.books.filter((book) =>
            book.title.toLowerCase().includes(searchTerm.toLowerCase()) ||
            book.author.toLowerCase().includes(searchTerm.toLowerCase()) ||
            book.genre.toLowerCase().includes(searchTerm.toLowerCase())
        );
    }
}

const bookCollection = new BookCollection();

// Example usage:
const book1 = new Book("Harry Potter and the Sorcerer's Stone", "J.K. Rowling", "Fantasy", 5, "Great re-read!");
const book2 = new Book("To Kill a Mockingbird", "Harper Lee", "Classics", 4, "A must-read");

bookCollection.addBook(book1);
bookCollection.addBook(book2);

console.log(bookCollection.getBooks()); // [book1, book2]

bookCollection.removeBook("Harry Potter and the Sorcerer's Stone");
console.log(bookCollection.getBooks()); // [book2]

console.log(bookCollection.searchBooks("to kill")); // [book2]
