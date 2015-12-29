var checkerboard = [[null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null],
                    [null,null,null,null,null,null,null,null]];
                    
function setSquare(player, row, col) {
    checkerboard[row][col] = player;
    return;
}

function getPieceAt(row, col) {
    return checkerboard[row][col] 
}

function clearBoard()   {
    for (x = 0; x < 8; x++)
        for (y = 0; y < 8; y++)
            checkerboard[x][y] = null;
    return;
}

function setUpRed() {
    for (x = 0; x < 3; x++)  {
        for (y = 0; y < 8; y++)
            if ((x + y) % 2 === 0)
                checkerboard[x][y] = 'R';
    }
    return;
}

function setUpBlack() {
    for (x = 5; x < 8; x++)  {
        for (y = 0; y < 8; y++)
            if ((x + y) % 2 === 1)
                checkerboard[x][y] = 'B';
    }
    return;
}

var pieces = {'red' : [],
              'black' : [] };
    
function getPiecesArray()   {
    var reds = 0;
    var blacks = 0;
    
    pieces = {'red' : [],
              'black' : [] };
              
    for (x = 0; x < 8; x++)
        for (y = 0; y < 8; y++) {
            if (checkerboard[x][y] === 'R') {
                pieces['red'][reds] = [x,y];
                reds++;
            } else if (checkerboard[x][y] === 'B') {
                pieces['black'][blacks] = [x,y];
                blacks++;
            }
        }
}

clearBoard();
setUpRed();
setUpBlack();
getPiecesArray();

  pieces['red'].map(function(piece){
      var row = piece[0];
      var col = piece[1];
      return checkerboard[row][col] === 'R';
    });

  pieces['black'].map(function(piece){
      var row = piece[0];
      var col = piece[1];
      return checkerboard[row][col] === 'B';
    });
