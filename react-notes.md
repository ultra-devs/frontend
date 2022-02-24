## using code mirror 
## here is the component

import './App.css';
import 'codemirror/theme/dracula.css';
import CodeMirror from '@uiw/react-codemirror';
import { useState } from 'react';


function App() {

  return (
 <div className="absolute top-20 bottom-40 left-20 right-20 text-left ">
          <CodeMirror
            value="console.log('hello  eclipse world!');"
            height="600px"
            width="700px"
            options={{
              theme: 'dracula',
              mode: 'js',
              dragDrop: true
            }}
            onChange={(value, viewUpdate) => {
              console.log('value:', value);
            }}
            />
        </div>
  );
}

export default App;
  
 ### dependency  
 "dependencies": {
    "@testing-library/jest-dom": "^5.16.1",
    "@testing-library/react": "^12.1.2",
    "@testing-library/user-event": "^13.5.0",
    "@uiw/react-codemirror": "^3.2.1",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "5.0.0",
    "web-vitals": "^2.1.4"
  }  
  
  index.js
  
  import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
