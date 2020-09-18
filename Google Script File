const url = "https://docs.google.com/spreadsheets/d/1IjwlzYsCgj0uqrcHEu5eBCcWAYHzkCSrUzXdCfEoTcQ/edit#gid=0";
const ss = SpreadsheetApp.openByUrl(url);
const ws = ss.getSheetByName("Data");

var bmi = 703*ws.getRange(ws.getLastRow(), 2).getValue() / (ws.getRange(ws.getLastRow(), 1).getValue() * ws.getRange(ws.getLastRow(), 1).getValue());

var list = ws.getRange(1, 1, ws.getLastRow(), 2).getValues;

function doGet(e) {
  var tmp = HtmlService.createTemplateFromFile("page");
  return tmp.evaluate();
}

function userClicked(userInfo){
  ws.appendRow([userInfo.uheight, userInfo.uweight, userInfo.uname]);
  bmi = 703*userInfo.uweight/(userInfo.uheight*userInfo.uheight);
}

function include(filename) {
  return HtmlService.createHtmlOutputFromFile(filename).getContent();
}

function getTableData() {
  
  var data = ws.getRange(2,1, ws.getLastRow()-1, 3).getValues();
  
  return data;
}
