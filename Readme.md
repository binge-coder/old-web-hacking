# What
These are html pages containing malicious scripts that perform denial of service attacks on whoever happens to open the html on their browsers.

# Will it work now
Back in 2020s, these hacks were quite effective. However, with modern browsers now equipped to minimize risks from malicious scripts, most of these vulnerabilities have been patched. But, if someone you know insists on using an outdated browser, you can still cause them some trouble by having them open one of these exploits on their browser. 

***TLDR*: They used to work when I was playing around with them a few years ago. Now they don't cuz web browsers are more secure.**

# Why
> I made these as part of my web development practical in college. These were the questions: 

1. **Endless alert**  
Create an HTML document that, when opened, displays a JavaScript alert dialog box. Each time the user dismisses the dialog box, a new, identical dialog box should appear, preventing interaction with the browser window.

   - You can put whatever text you want in the alert. (Be creative!)
   - To recover from this attack, it may be necessary to terminate your browser process.  
     - On Windows, use Task Manager (Ctrl+Alt+Del).  
     - On macOS, use Force Quit (Option-⌘-Esc).
   - Note that some browsers, such as Opera and Google Chrome, provide mitigations for this attack. Firefox does not.

2. **Whack-a-mole**  
Create an HTML page with a single button labeled "Click here". When clicked, the browser should open an infinite number of popup windows.

   - You can put whatever content you want in the popup windows.
   - Use a `data:` URL to give the popup window some content without making a network request.
   - Do not wait for the first window to close before opening the next one.
   - Your solution will be graded with the popup blocker on (default setting).
   - The windows need to visually open; it doesn’t count if the browser simply hangs.
   - You must open windows, not tabs.

3. **Sticky page**  
Create an HTML document that prevents the user from navigating away. If the user tries to enter a URL into the address bar, click a bookmark, or use the search box, the browser should remain at the same location no matter how many times the user tries.

   - You can put whatever content you want on the page.
   - The attack should work regardless of the URL where the page is located.
   - **Hint #1:** Try navigating the page in an `onunload` or `onbeforeunload` handler. Remove your handler to avoid creating an infinite loop.
   - **Hint #2:** Use `setTimeout` to delay navigation by a few milliseconds.
   - It is acceptable (but not required) if the browser’s progress indicator spins briefly before stopping. It should not keep spinning indefinitely.
