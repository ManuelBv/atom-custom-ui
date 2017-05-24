# atom-custom-ui
Style Atom text editor in order to allow you to see comments better


/* Atom custom UI styles - insert it in styles.less */

atom-text-editor {
  color: white;
  background-color: hsl(180, 24%, 12%);
}

// style UI elements inside atom-text-editor
atom-text-editor .cursor {
  border-color: #0f0;
}

atom-text-editor::shadow .gutter {
    background-color: #000;
    color: #fff;
}


.status-bar {
  color: white;
  background-color: black;
}

.tree-view {
  font-size: 12px;
  .list-item {
    line-height: 21px !important;
  }
  .selected:before, .selected:before {
    height: 18px !important;
  }
  .icon:before {
    font-size: 11px;
    width: 10px;
    height: 10px;
    opacity: .6;
    position: relative;
    top: 0px;
  }
  .header:before {
    font-size: 10px !important;
    opacity: .6;
    margin-right: 0px !important;
  }
}

/* more subtle invisibles */
.editor {
  .invisible-character {
    color: #504949;
    opacity: 0.5;
  }
  .indent-guide {
    opacity: .5;
  }
}


/* thicker cursor */
.editor .cursor {
  border-left-width: 2px;
}

.editor.is-focused .line-number.cursor-line-no-selection, .editor.is-focused .line.cursor-line {
    background-color: rgba(53, 57, 60, 0)
}

/* easier to see selection */
.editor.is-focused .selection .region {
  background-color: RGBA(100, 110, 100, 0.7);
  color: #fff !important;
  text-shadow: none;
}

/* html, js comments are easier to notice now */
atom-text-editor::shadow .comment {
  color: lightblue;
}


atom-text-editor::shadow .lines .line.cursor-line {
  background-color: RGBA(100, 110, 100, 0.7);
}

/* more visible gutter lines */

atom-text-editor::shadow .gutter .line-number.cursor-line  {
  background-color: blue;
  color: #fff;
}
