# React FFMPEG 🎬

#### Installation

```js
npm install react-ffmpeg

//or

yarn add react-ffmpeg
```

#### Usage

```js
import React, { Component } from "react";
import FFMPEG from "react-ffmpeg";

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {};
  }
  async componentWillMount() {
    console.log(FFMPEG.version);
    FFMPEG.init();
  }
  async onFileChange(e) {
    const file = e.target.files[0];
    FFMPEG.process(file);
  }

  render() {
    return (
      <input
        type="file"
        accept="audio/*,video/*"
        onChange={this.onFileChange}
      />
    );
  }
}

export default App;

```

## Roadmap 📈