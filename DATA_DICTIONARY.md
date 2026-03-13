# Features of the Spotify dataset

| Category | Feature | Description | Constraint/Range |
| -------- | ------- | ----------- | ---------------- |
| Metadata | `track_name` | Name of the song | String (non-null) |
| Metadata | `artist(s)_name` | Name of the artist(s) performing the song | String (non-null) |
| Metadata | `artist_count` | Number of artists contributing to the song | Integer (`≥1`) |
| Metadata | `released_year` <br> `released_month` <br> `released_day` | Release date details | Integer [`1900`,`2026`] <br> Integer [`1`,`12`] <br> Integer [`1`,`31`] |
| Metrics | `streams` | Total number of streams on Spotify | Integer (`≥0`) |
| Metrics | `in_spotify_playlists` | Number of Spotify playlists featuring the song | Integer (`≥0`) |
| Metrics | `in_spotify_charts` | Number of times the song appeared in Spotify charts | Integer (`≥0`) |
| Metrics | `in_apple_playlists` <br> `in_apple_charts` | Presence in Apple Music playlists and charts | Integer (`≥0`) |
| Metrics | `in_deezer_playlists` <br> `in_deezer_charts` | Presence in Deezer playlists and charts | Integer (`≥0`) |
| Metrics | `in_shazam_charts` | Number of times the song was recognized by Shazam | Integer (`≥0`) |
| Musicality | `bpm` | Tempo of the song (beats per minute) | Integer [`40`,`250`] |
| Musicality | `key` | Musical key | String {`C`,`C#`,`D`,`D#`,`E`,`F`,`F#`,`G`,`G#`,`A`,`A#`,`B`} |
| Musicality | `mode` | Major or Minor scale | String {`Major`,`Minor`} |
| Musicality | `danceability_%` | How danceable a song is | Float [`0`,`100`] |
| Musicality | `valence_%` | Positivity or happiness of the track | Float [`0`,`100`] |
| Musicality | `energy_%` | Intensity and activity level of the song | Float [`0`,`100`] |
| Musicality | `acousticness_%` | How acoustic a song is | Float [`0`,`100`] |
| Musicality | `instrumentalness_%` | Whether the song has vocals or is instrumental | Float [`0`,`100`] |
| Musicality | `liveness_%` | Likelihood of a song being recorded live | Float [`0`,`100`] |
| Musicality | `speechiness_%` | Presence of spoken words in the song | Float [`0`,`100`] |
