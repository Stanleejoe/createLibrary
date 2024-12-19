# createLibrary
function createLibrary() {  
    const books = [];  

    return {  
        addBook: function(title, author) {  
            const newBook = createBook(title, author);  
            books.push(newBook);  
        },  
        removeBook: function(title) {  
            const index = books.findIndex(book => book.title === title);  
            if (index !== -1) {  
                books.splice(index, 1);  
            } else {  
                console.log("Book not found.");  
            }  
        },  
        listBooks: function() {  
            if (books.length === 0) {  
                console.log("No books in the library.");  
            } else {  
                books.forEach(book => {  
                    console.log(book.details());  
                });  
            }  
        }  
    };  
}
