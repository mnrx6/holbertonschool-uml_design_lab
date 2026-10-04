# Class Diagram - Music Streaming Platform

## Classes

### User
Attributes:
- user_id: int
- name: str
- email: str

Methods:
- create_playlist()
- follow_artist()

### Artist
Attributes:
- artist_id: int
- name: str

Methods:
- get_albums()

### Album
Attributes:
- album_id: int
- title: str
- release_year: int

Methods:
- get_songs()

### Song
Attributes:
- song_id: int
- title: str
- duration: int

### Playlist
Attributes:
- playlist_id: int
- name: str

Methods:
- add_song()
- remove_song()

### Library
Attributes:
- library_id: int

Methods:
- add_song()
- add_album()
- get_saved_items()


## Relationships and Multiplicities

- Artist "1" -> "0..*" Album
  - One Artist can have zero or many Albums.
  - Each Album belongs to one Artist.

- Album "1" -> "1..*" Song
  - One Album contains one or many Songs.
  - Each Song belongs to one Album.

- User "1" -> "0..*" Playlist
  - One User can create zero or many Playlists.
  - Each Playlist belongs to one User.

- Playlist "0..*" <-> "0..*" Song
  - One Playlist can contain many Songs.
  - One Song can be added to many Playlists.

- User "0..*" <-> "0..*" Artist
  - One User can follow many Artists.
  - One Artist can be followed by many Users.

- User "1" -> "1" Library
  - Each User has one Library.
  - Each Library belongs to one User.

- Library "0..*" <-> "0..*" Song
  - A Library can contain many Songs.
  - A Song can be saved in many Libraries.

- Library "0..*" <-> "0..*" Album
  - A Library can contain many Albums.
  - An Album can be saved in many Libraries.


## Multiplicity Meaning

- "1" = exactly one
- "0..*" = zero or many
- "1..*" = one or many


## Relationship Symbols

- `-->` Association
- `o--` Aggregation
- `*--` Composition

