# Angular DropZone

## Getting Started

### Installation
Install the package using NPM.
```bash
npm install @shsf1382/file-input
```

## Usage / Examples
### Adding the module
Import the Module in your `app.module.ts` file:
```javascript 
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { FileInputModule } from '@shsf1382/file-input';
// Import the module

import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  
  imports: [BrowserModule, FileInputModule],
  // Import the module in "imports" as well
  
  providers: [],
  bootstrap: [AppComponent],
})
export class AppModule {}
```
### Adding the component
Add the Component in your `app.component.html` file:
```html 
<app-file-input [config]="myFileInputConfig"></app-file-input>
```
_Note: You can add the attribute binding of `[config]` to configure the component's behavior through the `myFileInputConfig` object. You can name this object as you wish._

### Configuring the options of the component
Configure the options in your `app.component.ts`:
```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})

export class AppComponent {
  myFileInputConfig: any = {
    maxFiles: '2',
    // Max files to be uploaded | Set to '10' by default

    allowedFileTypes: ['pdf', 'jpg', 'png', 'jpeg'],
    // Allowed file types | Set to ['jpg', 'jpeg', 'png'] by default

    maxSize: '10',
    // Max size for upload in MB | Set to '2' by default
    
    defaultImage: 'https://example-url.com/example.png',
    // Image to be dispalyed for non-image file types | Set to a default image
  };
}
```
_Note: You can set the value of `maxFiles`, `allowedFileTypes` & `maxSize` to `'noRule'`. This will remove the default rulesets of the component._

### More Detailed Document Coming Soon...