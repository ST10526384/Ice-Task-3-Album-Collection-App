# Album Collection App
This app is used for allowing a person to input/type information(e.g. artist, genre) about their fav music album. The app also checks if information has been inputed correctly
and stores the information that the person can see.


## Development Enviroment:
Here all the things I used to test and develop/rework the Album Collection App:

* Expo
* React Native
* TypeScript
* Institutional VM (Virtual Machine)
* BlueStacks 5
* Expo Go (Used the emulator)
* lastly I've installed @react-native-picker/picker

## Error Log:
Below is the error log

| Location | Problem | Error Type | Correction |
|----------|---------|-----------|-----------|
 | Picker import | they used @ui/community instead of basic picker classic | Import error  | Changed the import to @react-native-picker/picker and installed it |
 | Album type | year and rating were made as strings | TypeScript error | Changed them to number instead of string |
 | title length  | MIN && length was used incorrectly for the condition | Logical error| Use OR symbol  instead of  |
| artist length  | Used && | Logical error | Use OR symbol instead of && |
 | year range | numericYear < MIN_YEAR | Logical error | numericYear < MIN_YEAR then add the following after: OR symbol numericYear >  currentYear |
| rating range check | numericRating < 1 | Logical error | numericRating < 1 then add the following after: OR symbol numericRating > MAX_RATING |
 | handleSave | setAlbums([temporaryAlbum])  | Array error | setAlbums((current) => [...current, temporaryAlbum]) |
 | handleDelete | album.id === id | error | album.id !== id. |
| Picker selectedValue | selectedValue={title} | Logical error | selectedValue={genre} |
| Picker.Item value | value={genre}  | Logical and form error | value={item |
| FlatList keyExtracto | keyExtractor={(item) => item.title | Runtime error | keyExtractor={(item) => item.id |


## Testing
In brief I've tested the begin launch to see if the picker, form and etc if they were all there. I've tested the invalid messages you get for all the fields and checked if you can 
add a valid album as well. Lastly I checked if I can add more than one album and see if I can delete them. 

## Screenshot of App running:

## Conclusion:
In this ice task 3 I was able to try and find the errors in the code such as type script errors, picker import error and etc. However the most difficult or challenging errors were
the logical/ validating errors as you have to understand what it is trying to validate. After finding the errors I tested the app to see how it looks, how it runs and see if there were still errors 

