# Music Streaming Platform - Sequence Diagrams

## 1. Browse Songs and Albums

```mermaid
sequenceDiagram
    actor User
    participant Artist
    participant Album

    User->>Artist: get_albums()
    Artist-->>User: albums
    User->>Album: get_songs()
    Album-->>User: songs
```

## 2. Create a Playlist

```mermaid
sequenceDiagram
    actor User
    participant Playlist

    User->>User: create_playlist()
    User-->>Playlist: playlist created
```

## 3. Add a Song to a Playlist

```mermaid
sequenceDiagram
    actor User
    participant Playlist

    User->>Playlist: add_song()
    Playlist-->>User: song added
```

## 4. Remove a Song from a Playlist

```mermaid
sequenceDiagram
    actor User
    participant Playlist

    User->>Playlist: remove_song()
    Playlist-->>User: song removed
```

## 5. Save a Song to the Library

```mermaid
sequenceDiagram
    actor User
    participant Library

    User->>Library: add_song()
    Library-->>User: song saved
```

## 6. Save an Album to the Library

```mermaid
sequenceDiagram
    actor User
    participant Library

    User->>Library: add_album()
    Library-->>User: album saved
```

## 7. Follow an Artist

```mermaid
sequenceDiagram
    actor User
    participant Artist

    User->>User: follow_artist()
    User-->>Artist: artist followed
```

## 8. View User Playlists

```mermaid
sequenceDiagram
    actor User
    participant Playlist

    User->>Playlist: view playlists
    Playlist-->>User: user playlists
```

## 9. View Saved Songs and Albums

```mermaid
sequenceDiagram
    actor User
    participant Library

    User->>Library: get_saved_items()
    Library-->>User: saved songs and albums
```
