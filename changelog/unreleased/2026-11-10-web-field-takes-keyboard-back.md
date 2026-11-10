- **Web: a text field that gets the keyboard back takes it from the canvas, with its caret.** A
  frame where no field has the keyboard (a press that hits no field or lands on a window-drag
  strip, before the app hands focus back) moves DOM focus to the canvas. When a field had the
  keyboard again, the hidden textarea stayed unfocused: IME, dictation and the accent menu had
  nowhere to write, and the textarea's selection, which Chrome collapses to the start while it's
  unfocused, sent their text to the start of the field. A field now takes DOM focus back from the
  canvas and sets its selection again, as does a press on a field whose sync Rune skipped. Its
  input mode stays, so a touch screen's keyboard still waits for a tap.
