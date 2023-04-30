# Ardan Labs - Web4.0

## Laws of the Land
"Keep things simple until you can't"
"Determine the purpose of the logs"
"Always return concrete types"
"Prototype driven development, data oriented design"
"If you don't understand the data you don't understand the problem"
"Comments are code - treat them as such"
"We don't make things easy TO DO, we make things easy TO UNDERSTAND"

## Repo Structure (No more than 5 layers)

1. app 
   - can import from business, foundation, vendor
   - binaries of the project
   - allowed to log
   - start up, shut down, any code receiving external input, sending external output
   - independent data models
2. business
   - can import from foundation, vendor
   - packages specific to the business problem
   - allowed to log
   - core
   - data - database schema, service
   - sys - database access, lower level validation
   - web
3. foundation
   - can import from vendor
   - ‘std lib’ of project
   - not allowed to log
   - not dependent on each other
   - could potentially become third party dependencies
4. vendor
   - third party modules/dependencies
5. zarf
   - bottom of the tree
   - container configuration

## makefile - self-documenting on how to onboard into project

## fun ideas
Vendor new modules
go get -u -t -d -v ./..
^ weekly github action to issue PR?
