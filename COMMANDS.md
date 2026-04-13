📂 (Navigation & File System)

“ls”
Mówi co jest w folderze, ale nie co jest w srodku plikow.

    “ls -a” - pokazuje ukryte pliki

    “ls -l” - shows accesibility, owner, size

“cd”
Przechodzi miedzy folderami:

    “cd ..” - przejscie o jeden poziom wyzej w katalogu

    “cd” - powrot do poczatkowego katalogu

    “cd -” - powrot do poprzedniego katalogu

    “cd /” - przejscie do glownego katalogu na dysku (root)

“file”
Przed użyciem “cat” warto użyć file, poniewaz plik moze byc skompresowany, przez co samo cat wyswietli losowy kod.

    file nazwa_pliku

    file ./* - jesli jest wiele plikow wpisanie tej komendy pokaze CZYM sa te pliki

🔍 (Searching)

“find”
Nie wyswietla tresci pliku, ale mowi gdzie konkretnie jest. no uzywajac find . -size 1033c (szuka sie pliku specyficznego) find pokazuje gdzie jest a potem mozna uzyc “cat” do odszyfrowania tego pliku.

If there is group or user you can use them to find the file you are looking for:

    “find -user X -group Y”

Also you can add size of the file:

    “find -user X -group Y -size Zc 2>/dev/null”
    Adding “2>/dev/null” is necessary, because it filters wrong files.

“du”
“Disk usage” pokazuje ile miejsca zajmuja pliki i foldery, przyda sie przy szukaniu pliku o specyficznej wadze.
📄 (Content Extraction)

“cat”
Czytnik, narzedzie do zagladania do srodku pliku, uzywa sie gdy wie sie, ze w danym pliku jest hasło:

    cat nazwa_pliku

    “cat ./-” - used for weird files names

“strings” - shows lines that contain minimum 4 characters (numbers, letters, signs), for example some programmers leave binary data with regular data.
🛠️ (Text Manipulation & Filtering)

“grep” - shows ONLY lines that mention word that I am looking for.

    “cat data.txt | grep "millionth"”

“tr” - translate, changing some characters for other ones, for example to change a for A and z for Z:

    cat file | tr ‘a-z’ ‘A-Z’

“sort” - sort lines alphabetically or numerically
some of commends such as uniq are required to be “sort” so they work better

“uniq” - deletes copies of lines and only leaves one of many

    “uniq -u” - shows lines that occur only ONE TIME in whole file

🔐 (Decoding & Hex)

“base64” - coding and decoding in format Base64 (ends with ==), for example:

    “base 64 -d “file”” - decoding some file

“xxd” - makes hexdump - shows whats inside 16-code file

    to make file binary again use “xxd -r” (“r” as reversed”)

📦 (Archives & Compression)

“tar” - combining many files in one (archives)

    to decompress: “tar -xf file.tar”

“gzip” or “gunzip”

    to decompress: “gunzip file.gz”

“bzip2” or “bunzip2”

    to decompress: “bunzip2 file.bz2”

⚙️ (Other commands & Operators)

“|” - pipe, used when wants to combine two commends

“\” - escape, used when file has two parts for example:

    “moje haslo.txt” you should use: “cat moje\ haslo.txt”

“/” :
Used to separate things for example:

    “cd var/lib” tells terminal to enter var first then lib
    Used to represent the root directory (top level of the system).
