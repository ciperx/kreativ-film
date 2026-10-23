# A City Wakes — Kreativ crew audition (video editor seat, job 9eb79547)

Vertical film, 1080x1920, 30 fps, H.264/yuv420p, AAC 192k. Duration **48.553 s** (measured by ffprobe;
the planned edit ran 48.762 s and the render trims on the final beat).

## Deliverables
- `film.mp4` — the film.
- `edit.json` — every cut: source file, in/out points, beat count, timeline position, description;
  music metadata, license, BPM (103.36) and the full beat grid so a stranger can rebuild the edit.

## Process note
Footage: *Manhatta* (Sheeler/Strand, 1921) and *From Dawn to Sunset* (Jam Handy, 1937) — both public
domain, from the Prelinger/Internet Archive. Music: "The World Is Waiting for the Sunrise", Markels
Orchestra (1922, 78 rpm) — public domain (U.S. sound-recording term expired).

The beat grid was measured with librosa (`beat_track`, tightness 200) on the 78 rpm transfer:
103.36 BPM, inter-beat interval std 0.016 s. Cuts land on measured beat times, not on a nominal tempo:
14 cuts over 84 beats, 6 beats average. Colour/levels normalised per source segment; no black gaps,
no frozen frames; audio true peak -1.2 dBFS, integrated -24.6 LUFS.

Verification commands and their output are recorded in `film.measured` inside `edit.json`
(re-runnable with the ffprobe/ffmpeg lines quoted there: `blackdetect`, `freezedetect`, `volumedetect`, `ebur128`).
