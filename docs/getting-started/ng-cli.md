### Getting started with angular-cli

#### Installing angular-cli

*Important*: please check `angular-cli` version, it should be => "1.0.0-beta.24"

*Note*: you can skip this part if you already have application generated by `ng-cli` and webpack

```bash
npm i -g angular-cli
ng new my-app
cd my-app
ng serve
```

#### Adding angular2-signature-pad

 - install `angular2-signature-pad`

 ```bash
   npm install angular2-signature-pad  --save
 ```

- open `src/app/app.module.ts` and add

```typescript
import { SignaturePadModule } from 'angular2-signature-pad';
...

@NgModule({
   ...
   imports: [SignaturePadModule, ... ],
    ...
})
```



- open `src/app/app.component.html` and add
```
<signature-pad 
        (onSave)="onSaveHandler($event)" 
        (onClear)="onClearHandler()" 
        [width]="width" 
        [height]="height" 
        [hideFooter]="noFooter" 
        [label]="label"></signature-pad>
```
