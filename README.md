# How to Show the Watermark Text in GridNumericColumn of WPF DataGrid?

This sample show cases how to show the watermark text in the [WPF DataGrid](https://www.syncfusion.com/wpf-controls/datagrid) (SfDataGrid).

You can show the `PlaceHolderText` for `GridNumericColumn` by loading the `SfNumericTextBox` as `GridNumeriColumn.CellTemplate` in `DataGrid`.

``` c#
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