db.books.insertOne({
  title: "Книга 1",
  description: "Описание 1",
  authors: "Автор 1"
});


db.books.insertMany({
  title: "Книга 2",
  description: "Описание 2",
  authors: "Автор 2"
},
{
  title: "Книга 3",
  description: "Описание 3",
  authors: "Автор 3"
},
);


//Должен вернуть книгу 3
db.books.find(
{title {$ eq :  "Книга 3"} },
);

//Должен вернуть все книги
db.books.find({}},
);



db.books.updateOne(
    {_id: {$lt: 1}},
    {$set: {description: description, authors: authors}}
);
