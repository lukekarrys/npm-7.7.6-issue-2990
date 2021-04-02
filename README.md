This example uses [volta](https://docs.volta.sh/guide/) to switch `npm` versions.

**npm@7.7.6**
```
> volta pin npm@7.7.6
success: pinned npm@7.7.6 in package.json

> npm run echo -w package1

> package1@1.0.0 echo
> echo "test"

test

> npm run run:echo -w package1

> package1@1.0.0 run:echo
> npm run echo

npm ERR! No workspaces found:
npm ERR!   --workspace=package1

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/lukekarrys/.npm/_logs/2021-04-02T23_31_38_891Z-debug.log
npm ERR! Lifecycle script `run:echo` failed with error: 
npm ERR! Error: command failed 
npm ERR!   in workspace: package1@1.0.0 
npm ERR!   at location: /Users/lukekarrys/Desktop/test/packages/package1
```

**npm@7.8.0**
```
> volta pin npm@7.8.0
success: pinned npm@7.8.0 in package.json

> npm run echo -w package1    

> package1@1.0.0 echo
> echo "test"

test

> npm run run:echo -w package1

> package1@1.0.0 run:echo
> npm run echo


> package1@1.0.0 echo
> echo "test"

test
```