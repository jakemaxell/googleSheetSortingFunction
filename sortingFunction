function sort() {
  
  var ss = SpreadsheetApp.getActiveSpreadsheet();

  var firstSheet = ss.getSheetByName("Recruiting List");
  var secondSheet = ss.getSheetByName("Rejections");
  var thirdSheet = ss.getSheetByName("Hires");

  var lastRow = firstSheet.getLastRow() + 1;
  var col = 13;
  var test = 0;

  for(var x = 1; x < 1000; x++){

    if(firstSheet.getRange(x, col).getValue() == "N" || firstSheet.getRange(x, col).getValue() == "n"){
      test += 1;
      
      var nextRow = secondSheet.getLastRow() + 1;
      var getCopyRange = firstSheet.getRange("C" + x + ":O" + x);
      getCopyRange.copyTo(secondSheet.getRange(nextRow, 2));

      firstSheet.insertRowAfter(x);
      firstSheet.deleteRow(x);
      //firstSheet.insertRowAfter(x);
      
    }
    else if(firstSheet.getRange(x, 13).getValue() == "Y" || firstSheet.getRange(x, col).getValue() == "y"){
      test += 1;
      
      var nextRow = thirdSheet.getLastRow() + 1;
      var getCopyRange = firstSheet.getRange("C" + x + ":O" + x);
      getCopyRange.copyTo(thirdSheet.getRange(nextRow, 2));

      firstSheet.insertRowAfter(x);
      firstSheet.deleteRow(x);
      //firstSheet.insertRowAfter(x);
    }

    Logger.log(test);

  }
  

}
