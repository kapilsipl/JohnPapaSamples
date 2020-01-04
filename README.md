# JohnPapaSamples
Angular CLI options 

npm i -g @angular/cli
	Install angular cli globally
ng -v 	Check version of Angular
ng new ngtest	New Angular project
ng new ngtest --skip-install	"Create new Angular aplication, --skip-install is stop to install npm in folder
http://prntscr.com/qj6ht9"
ng new my-app --dry-run	Don't write the files, but report them (it will show how many files will generate but not generate)
ng new --help	All options of new command
ng new my-app --prefix sipl --skip-install	It will change the prefix from app-root to sipl-root
ng new my-app --skip-tests --prefix sipl --skip-install	"It will skip .spec.ts files from the component 
http://prntscr.com/qj6mcu"
ng new my-app --skip-tests --prefix sipl --skip-install --style scss	To generate project with scss file
ng new my-app --routing --skip-tests --prefix sipl --skip-install --style scss	To add the routing in project
Common	http://prntscr.com/qj6pky
Best practices	http://prntscr.com/qj6pt2
ng lint my-app --help	Show the help for linting a project
ng lint my-app -format stylish	Lint and format the output (with color i.e red for bug)
ng lint my-app -fix	Lint and attempt to fix all problems (before do that make sure all of your changes will be git stash (to save)
	
Blueprints	
ng generate <blueprint> <options>	generate code
ng generate component customer	customer.component.ts & it's associate files
ng generate service customer-data	customer-data.service.ts & it's associate files
ng generate class customer-model	customer.model.ts & it's associate files
	
Generate components	
Aliases as Shortcuts	
use the 'g' alias as a shortcut for generate	ng g c customer
use the 'c' alias as a shortcut for component	
--flat	Should a folder be created?
--inline-template (-t)	Will the template be in the .ts file
--inline-style (-s)	Will the style be in the .ts file?
--spec	Generate a spec?
--view-encapsulation (-v)	View encapsulation strategy
--change-detection (-c)	Change detection strategy
--dry-run (-d)	Report the files, don't write them
	
ng generate component pet (ng g c pet)	With spec & css/scss file
ng generate component pet --inline-template --inline-style (ng g c pet -t -s)	Without spec & css/scss file
ng g c pet -ts	We can stack the aliases (combine the command)
ng g c pet --flat	Not create the folder just create the file onlye
ng g c pet --inline-template	Put the template in the .ts file, not create new HTML file
ng g c pet --inline-style	Put the css in the .ts file, not create new CSS file
ng g c pet --prefix kpl	Prefix the component with kpl-
ng g c pet -st --flat --prefix kpl	Stack all command in single (combine all aliases)
	
Guard	Gard is adding for permission (roles and permission)
ng g guard auth	canActivate guard auth.guard.ts
	
ng build	output to dist/[appname]
runtime.js	WebPack runtime
main.js	AppCode
polyfills.js	Plateform polyfills (browser compitablity for es code)
styles.s	Styles
vendor.js	Angular & other vendor files
	
Exploring the source in the Output	
in folder - npm install webpack-bundle-analyzer --save-dev	
ng build --stats-json	https://github.com/webpack-contrib/webpack-bundle-analyzer
npx webpack-bundle-analyzer dist/my-app/stats.json	
	
npm install source-map-explorer --save-dev	
ng build	https://github.com/danvk/source-map-explorer
npx source-map-explorer dist/my-app/main.js	
	
