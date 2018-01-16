﻿# Examples for FlexCel Studio for .NET

Here you can find all the demos for [FlexCel Studio for .NET](http://www.tmssoftware.com/site/flexcelnet.asp)

You can find a description of each demo in the [documentation](http://www.tmssoftware.biz/flexcel/doc/net/index.html)
**All the demos here are also available when you install FlexCel using the setup.**

**:book: Note** We update this repository automatically every time we release a new FlexCel version. So if you have notifications integrated with github, you can subscribe to this feed to be notified of new releases.


## New on v 6.18.5.0 - January 2018


- **New convenience methods SetCellValue(cellRef, value) and GetCellValue(cellRef).** The new methods [SetCellValue(cellRef, value)](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/ExcelFile/SetCellValue.html#excelfileSetcellvaluestring-object) and [GetCellValue(cellRef)](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/ExcelFile/GetCellValue.html#excelfilegetcellvaluestring) allow you to set or get a cell value directly from a text reference like "A1" without having to use a [TCellAddress](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/TCellAddress/index.html) class.

- **Support for shape connectors in xlsx.** Now FlexCel will preserve connections between shapes in xlsx, and convert them from xls to xlsx and viceversa. We've also added the properties [IsConnector](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/TShapeProperties/IsConnector.html)  [StartShapeConnection](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/TShapeProperties/StartShapeConnection.html) and [EndShapeConnection](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Core/TShapeProperties/EndShapeConnection.html) to allow you to enter connections with the API. As usual, APIMate will tell you the code needed to add a connector from an Excel file.

- **Bug Fix.** The VLOOKUP and HLOOKUP functions now support wildcards (* and ?) in search strings.

- **Improved compatibility with invalid files generated by third party tools.** Some xlsx generators can write invalid column widths. Now when exporting to html/pdf, FlexCel will consider those widths as default (like Excel does) and not 0 (as it used to do).

- **Bug Fix.** FlexCel could fail to parse some structured references in tables.

- **Bug Fix.** When calculating UDFs and there were errors in the arguments, FlexCel could in some cases return #ERRNAME! instead of evaluating the UDF.

- **Bug Fix.** In some files the calculated height for items inside Forms Listboxes was too big.

- **Bug Fix.** FlexCel failed to read custom document properties saved in UTF16.

- **Bug Fix.** Reports with [DeleteEmptyBands](http://www.tmssoftware.biz/flexcel/doc/net/api/FlexCel.Report/FlexCelReport/DeleteEmptyBands.html) = TDeleteEmptyBands.ClearDataOnly would not clear text inside textboxes or hyperlinks.

- **Bug Fix.** In some bidirectional reports with report.DeleteEmptyBands = TDeleteEmptyBands.MoveRangeUp the tag text was not erased.

