[![Coverage Status](https://coveralls.io/repos/github/React-Sight/React-Sight/badge.svg?branch=master)](https://coveralls.io/github/React-Sight/React-Sight?branch=master)
[![Build Status](https://travis-ci.org/React-Sight/React-Sight.svg?branch=master)](https://travis-ci.org/React-Sight/React-Sight)
[![Chrome Web Store](https://img.shields.io/chrome-web-store/users/aalppolilappfakpmdfdkpppdnhpgifn.svg)](https://chrome.google.com/webstore/detail/react-sight/aalppolilappfakpmdfdkpppdnhpgifn)
[![Chrome Web Store](https://img.shields.io/chrome-web-store/v/aalppolilappfakpmdfdkpppdnhpgifn.svg)](https://chrome.google.com/webstore/detail/react-sight/aalppolilappfakpmdfdkpppdnhpgifn)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
# React Sight
<img src="/assets/sidewaylogo4.png" width="300"/>
React Sight is a live view of the component hierarchy tree of your React application with support for React Router and Redux.

<p align="center">
  <img src="/assets/testingDEMO.gif">
</p>


### We are currently working on squashing bugs related to fiber


## Set Up | Install From Chrome Store

1. Make sure you've added [React Dev Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) to Chrome. 

2. Install [React Sight](https://chrome.google.com/webstore/detail/react-sight/aalppolilappfakpmdfdkpppdnhpgifn) from the Chrome web store

3. If you are running local file URLs, make sure to enable "Allow access to file URLs" in the extension settings for both React Dev Tools and React Sight

4. Run your React application, or open (almost!) any website running React!

5. Open Chrome Developer Tools (cmd+opt+j) -> React Sight panel

## Building Your Own Version

If you'd like to build your own version of React Sight:

1. Clone the repo and `npm install` dependancies

2. Use `npm start` to generate the build 

3. In Chrome, open the extensions tab and click 'Load Unpacked Extension'. Load the folder '~/ReactSight/chrome-ext'

If you have any additional questions send us a message at reactsight@gmail.com :)

## Usage

Hover over nodes to see their state and props in the side panel. 

Hide DOM elements, Redux components, and Router components with the built in filters, so that you can focus only on the components you've written

Zoom in by double clicking, and zoom out by shift + double clicking (mousewheel zoom coming soon!)

## Why?

We built React Sight because there are no tools on the market that give you a visual representation of the structure of your App. When we were developing our own projects, we wished we had a way to see how everything was structured.

We wanted React Sight to be simple to use, which is why all you have to do is install a Chrome extension. No modifying your existing code!

## How Does It Work?

When the dev tools are opened, React-Sight searches for React renderer's, and patches the render to collect data on each state change.

Data is posted to the Window, where it is read by Chrome's background.js window, and is then relayed to React-Sight's devTools page.

The raw data is then processed and fed to D3, where it is displayed to the user.

## Troubleshooting

'React not found' or no data:

Sometimes React-Sight doesn't get a snapshot of the data at load, triggering a setState ussually fixes this

Maximum call stack exceeded and other console errors:

This is a bug where the parsing functions get stuck in an infinite loop. We are working on a fix.

## Testing

Run `npm test` to run the test suite

## Contributing

Found a bug? Have a suggestion? Want to make React-Sight better?

Please submit issues/pull requests if you have feedback or would like to contribute. If you're interested in joining the React Sight team as a contributor, feel free to message one of us directly, or just start submitting pull requests!

## Authors

David C Sally (https://github.com/davidcsally)

Grant Kang (https://github.com/Grant05)

William He (https://github.com/hewilliam)

## Contact

Like our app? Found a bug? 

Tell us what you think!

reactsight@gmail.com

Visit us at www.reactsight.com

## Roadmap 

Here's our top development priorities

1. Better support across all React versions, especially fiber
2. More consistent detection of root nodes when React Sight is opened
3. Support for multiple React Applications / mounting nodes 
4. More robust error handling and guard blocks for extracting state, props, and store
5. Logging / Debugging mode for development, feedback, and error reporting
6. Performance and stability updates
7. Mousewheel zoom in D3 chart (if you can solve this I will order you 🍕)
8. UX improvements
9. Improved documentation
10. Hook into React DevTool's reporting so that we don't have to reimplement it :)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
