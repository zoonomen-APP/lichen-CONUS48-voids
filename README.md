# Void maps — where the lichen record is silent

Forty-eight sheets, one per state of the conterminous United States, showing
where the Consortium of Lichen Herbaria holds records and where it holds
none.

Open `index.html` to step through them. Arrow keys move between states, the
selector jumps, and states marked with an asterisk carry a written note
alongside the map.

## Reading a sheet

Each sheet divides the state into hexagonal cells about 18 km across. A cell
is one of two things and never both.

**Cyan** — the cell holds at least one record. Brightness is the number of
specimen records, on a log scale, running to that state's own densest cell.

**Blue through yellow** — the cell holds no record. Colour is the
distance from that cell to the nearest cell that does hold one, running to
that state's own maximum.

The two are separate measurements with no conversion between them. The eye
fuses them into a single sense of how well known the ground is, which is a
fair reading, but only as an ordering: the map supports "this is better known
than that" and does not support arithmetic.

**Red diamond** — the centre of the largest record-free circle in the state.
Not the deepest point of anything; the cells are all equally empty. It marks
the middle of the biggest hole, and the number beside it is that hole's
radius.

**Blue diamond** — the cell holding the most specimen records that meet the
requisite requirements.

Either diamond is omitted where it would be marking a tie rather than a
standout. Four states have no record-free cells at all at this grain and say
so on the sheet.

Coordinates for both diamonds appear in the subtitle and, in the viewer, link
to OpenStreetMap.

## What an empty cell means

**No records meeting study requirements produced.**

That sentence is doing precise work. It does not say nobody has collected
there. It says the Consortium holds no record, carrying coordinates, passing
the study's name filter, that places a specimen record in that cell. A specimen may
sit in a cabinet undatabased, be in the database without coordinates, have
a locality too vague to georeference, or it may be determined only to genus.

The colour scale on each sheet runs to that state's own range, so the same
yellow means 110 km in Texas and 20 km in Washington. The ceiling is stated
in the subtitle of every sheet. Cross-state comparison belongs in
`state_void_summary.tsv`, not in the colours.

## Files

    index.html                  the viewer
    grand_void_<ST>.png         one sheet per state
    notes/<ST>.md               commentary, where written
    state_void_summary.tsv      per-state statistics for all 48

## Method and caveats

See `../docs/void_method.md` for how the sheets are made, what the query
admits, and what the analysis cannot tell you — including a sensitivity test
showing what changes when the grid changes, and a caution about survey plots
that behave differently from ordinary collecting.

Nothing in the method is lichenological. It reads coordinates from a database
and reports where there are none. The method document describes the approach
in enough detail to be reimplemented; the scripts themselves are not
published, for reasons given there.
