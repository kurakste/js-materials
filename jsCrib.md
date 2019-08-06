Arrays:
---
uniq = [...new Set(array)];

Profiling
---
1) 
  After some initial playing around with --prof I found it easier to use Chrome's DevTools. At least for the JavaScript side.             
  DevTools has the advantage of being interactive, and allows you to drill into the underlying .ts code.

  1)  Start your app with node's --inspect flag:
    node -r ts-node/register -r tsconfig-paths/register --inspect ./src/index.ts
    (Here I'm using ts-node + tsconfig-paths for the typescript handling)
  2)  Open chrome://inspect in Chrome
    Under "Remote Target" click "inspect" for your new target
      
  (This should open up a Chrome inspector window connected to your app)
  Go to the "Profiler" tab and begin recording a new profile
  
2) node --prof-process isolate-0xnnnnnnnnnnnn-v8.log > processed.txt

nodejs on mac:
---
sudo chown -R `whoami`:admin /usr/local/include/node
sudo chown -R `whoami`:admin /usr/local/bin
sudo chown -R `whoami`:admin /usr/local/share


