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
