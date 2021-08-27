<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/209830985/20.2.6%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T816800)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Index.razor](./CS/DataGridBindingToDataTable/Pages/Index.razor)
<!-- default file list end -->

### Blazor Data Grid - How to bind a grid to a DataTable object

DxDataGrid can be bound only to the IEnumerable collection of objects. So, a DataTable object cannot be directly passed to the *DxDataGrid.Data* property.


In the case when the structure of the used DataTable is known, it's possible to create a class with corresponding properties for each column in the DataTable object. Then it's necessary to generate the IEnumerable collection of this class' objects based on the *Rows* collection of the DataTable object. 
This approach is demonstrated in the first "Static object" grid.


In some cases, the DataTable object is generated dynamically and its structure is not known. For this scenario, our DxDataGrid supports binding to the IEnumerable collection of the [ExpandoObject](https://docs.microsoft.com/en-us/dotnet/api/system.dynamic.expandoobject?view=netframework-4.8) objects. It's possible to dynamically generate properties in such objects based on the structure of the used DataTable. 
This approach is demonstrated in the second "Dynamic object" grid. Check the [ConvertDataTableToExpandoObjectList](./CS/DataGridBindingToDataTable/Pages/Index.razor#L66) method which converts the DataTable object to the IEnumerable collection of the ExpandoObject objects.
