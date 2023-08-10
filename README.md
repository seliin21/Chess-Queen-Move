# Chess-Queen-Move
""" In this mini game where we imagine the chessboard, the queen can move to any number of cells vertically, horizontally, and diagonally. You can easily check whether the queen can move to the desired position by entering the current position as row and column, and specifying the target position also as row and column. """

def queen_move():
    
    x = int(input("Enter the row of the first square (1-8): "))
    y = int(input("Enter the column of the first square (1-8): "))
    x_target = int(input("Enter the row of the target square (1-8): "))
    y_target = int(input("Enter the column of the target square (1-8): "))
    
    if not (1 <= x <= 8 and 1 <= y <= 8 and 1 <= x_target <= 8 and 1 <= y_target <= 8):
        print("Invalid input. Column and row numbers should be between 1 and 8.")
        return
    
    # If the queen moves vertically or horizontally:
    if x == x_target or y == y_target:
        print("YES.")
        
    # If the queen moves diagonally:
    if abs(x - x_target) == abs(y - y_target):
        print("YES.")
        
    else:
        print("NO.")
        
queen_move()
