This initializes a JBrowse instance in a React app

This uses a number of crutches that are not necessarily ideal, and could possibly be fixed up, but help for now


This includes


1) copying img directory from jbrowse github to public folder. the jbrowse distribution does not copy it's img to the dist directory, making it so the dist directory of jbrowse is not self contained

2) manually having a jbrowse.conf and jbrowse_conf.json empty in the public folder. jbrowse does not currently, as of writing, work without these files there. it should have an option to initialize from a config passed to browser instance only though

3) it uses the "JBrowse CDN", e.g. just a script tag pointing to jbrowse.org/code/JBrowse-1.16.9/dist/browser.bundle.js, instead of say a @gmod/jbrowse npm package



Despite these things, the instance works and is maybe an example you can build on
