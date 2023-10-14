1. Запрос(ы) для вставки данных минимум о двух книгах в коллекцию books:
   db.books.insertMany(
   [
   {
   title: "Book3",
   description: "Description Book3",
   authors: "Book3 author"
   },
   {
   title: "Book4",
   description: "Description Book4",
   authors: "Book4 author"
   }
   ]
   )

2.Запрос для поиска полей документов коллекции books по полю title:

db.books.find(
{title: "<название книги>"}
)

3. Запрос для редактирования полей: description и authors коллекции books по \_id записи:
   db.books.update(
   { \_id: ObjectId("<ID книги>") },
   {
   $set: {
   description: "Новое описание",
   authors: "Новые авторы"
   }
   }
   )
