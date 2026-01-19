# How to Show the Watermark Text in GridNumericColumn of UWP DataGrid?

This sample show cases how to show the watermark text in the [UWP DataGrid](https://www.syncfusion.com/uwp-ui-controls/datagrid) (SfDataGrid).

You can show the `PlaceHolderText` for [GridNumericColumn](https://help.syncfusion.com/cr/uwp/Syncfusion.UI.Xaml.Grid.GridNumericColumn.html) by loading the [UWP NumericTextBox](https://www.syncfusion.com/uwp-ui-controls/numeric-textbox) (SfNumericTextBox) as [GridNumeriColumn.CellTemplate](https://help.syncfusion.com/cr/uwp/Syncfusion.UI.Xaml.Grid.GridColumnBase.html#Syncfusion_UI_Xaml_Grid_GridColumnBase_CellTemplate) in `DataGrid`.


#### XAML
``` xml
<syncfusion:SfDataGrid x:Name="dataGrid"
                    AllowEditing="True"
                    AllowFiltering="True"
                    AllowGrouping="True"
                    AllowDeleting="True"
                    AllowSorting="True" 
                    ColumnSizer="Star"
                    AutoGenerateColumns="False"
                    ItemsSource="{Binding Emp}"
                    ShowGroupDropArea="True">
 
    <syncfusion:SfDataGrid.Columns>
            <syncfusion:GridNumericColumn.CellTemplate>
                <DataTemplate>
                    <input:SfNumericTextBox Value="{Binding Salary,Mode=TwoWay}" PlaceholderText="Type Here" AllowNull="True"/>
                </DataTemplate>
            </syncfusion:GridNumericColumn.CellTemplate>
        </syncfusion:GridNumericColumn>
        <syncfusion:GridTextColumn MappingName="SickLeaveHours"/>
    </syncfusion:SfDataGrid.Columns>
 
</syncfusion:SfDataGrid>
```

Take a moment to peruse the [UWP DataGrid - Getting Started](https://help.syncfusion.com/uwp/datagrid/getting-started) documentation, where you can find about DataGrid with code examples.