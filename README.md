# Asyncc-Inn
Author: Ameilia Valdes, 1/25/2021
![ERD Image]()

1. The Location table will hold each hotel location. it has a primary location id, and have columns for the name, city, state, address, phone number and number of rooms for each location. it has a one to one relationship with the join table LocationRoom.
2. The LocationRoom table is a join table with a payload that is the price of each room. It uses the Location ID and Room ID as foreign keys and has a third collumn that is the price. it has a one to one relationship with the room table. 
3. The room table has a primary room id, and collumns for the room number, a pet friendly bool, and an enumerable nickname of the room. This table is joined to the LAyout by Nickname table using the room layout table.
4. The Layout by Nickname talbe has a primary key, and collums for the room Id, brought in as a foreign key, a collumn for ammenities, how many bedrooms it has, and the actual nickname. This table is joined to the room table with the RoomLayout table. This table has a one to many relationship with rooms, because many rooms can share a nickname.
5. The RoomLayout table joins the room and layout tables using their ID's as composite keys. This will assure that the room has the data it needs from it's nickname(ammenities, number of bedrooms), which will be used later for determining the price of the room.