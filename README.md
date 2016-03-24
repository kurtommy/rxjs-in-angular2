## RxJS in Angular 2

## Notes
Typings for Angular 2 and RxJS to work with static files:
`typings install`
vendor:
`wget --include 2.0.0-beta.11 --mirror --execute robots=off --no-host-directories --cut-dirs=1 --reject="index.html*" --continue https://code.angularjs.org/2.0.0-beta.11`
vendor/tools
`wget --include tools --mirror --execute robots=off --no-host-directories --cut-dirs=1 --reject="index.html*" --continue https://code.angularjs.org/tools`

## Unscripted:
Yes, this is a lot of work to avoid npm. If you want to script it, be my guest! :)

You need `npm install dts-generator typescript -g`:
`git clone https://github.com/ngrx/store.git`

changes to `tsconfig.json`:
```
"module": "system",
"outFile": "ngrx.js",
```

run `tsc` which will output `ngrx.js`
changes to `ngrx.js`
```
"index" become "@ngrx/store"
```

run `dts-generator --project ./ --out ngrx.d.ts`
changes to `ngrx.d.ts`
```
"index" become "@ngrx/store"
```

$('.form-control.filename').each(function(i){
  $('.form-control.filename')[i].value = $('.form-control.filename')[i].value.replace(/_/g, '\\');
});
$('.btn.btn-primary')[0].click()

https://npmcdn.com/@reactivex/rxjs@5.0.0-beta.3/dist/global/Rx.js

01 - Rendering an Observable with the Async Pipe - https://gist.run/?id=2ea9cca663c9032fb8aa
