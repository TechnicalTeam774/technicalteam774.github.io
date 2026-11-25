# RRN Check — Settlement Verification

Matches Kashier transaction flags against bank merchant statements, on RRN first —
the one reference that never repeats — then on merchant number + card + amount,
then on merchant name + card + amount.

## How your data is handled

Nothing is uploaded. Every file you add is read inside your own browser and stored
in that browser only (IndexedDB). Other people opening this page see their own data,
never yours.

## Moving your statements between machines

- **Back up statements** writes every loaded statement into one `.rrnbak` file.
- **Restore backup** reads that file back in, on any machine.

Use this to bring statements over from the older local copy of the tool.
