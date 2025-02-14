In Angular apps, you can use [HttpInterceptor](https://angular.io/api/common/http/HttpInterceptor) to intercept Ajax requests in DevExtreme components such as [DataSource](/api-reference/30%20Data%20Layer/DataSource '/Documentation/ApiReference/Data_Layer/DataSource/'), [FileUploader](/api-reference/10%20UI%20Components/dxFileUploader '/Documentation/ApiReference/UI_Components/dxFileUploader/'), and [Map](/api-reference/10%20UI%20Components/dxMap '/Documentation/ApiReference/UI_Components/dxMap/'). This task requires that you import `DxHttpModule`.

---
##### Angular

    <!-- tab: app.component.ts -->
    import DataSource from 'devextreme/data/data_source';
    import ODataStore from 'devextreme/data/odata/store';
    import { DxHttpModule } from 'devextreme-angular/http';

    @Component({
        selector: 'app-root',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css'],
        providers: [],
        imports: [DxHttpModule],
    })

    export class AppComponent {
        dataSource = new DataSource({
            store: new ODataStore({
                version: 2,
                url: 'http://www.example.com/Northwind.svc',
            }),
        });

        constructor() {
            // ...
        }
    }

---