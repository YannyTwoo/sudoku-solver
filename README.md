# SolveSudoku
SolveSudoku extract and solve sudoku from image. It uses a collection of image processing techniques and Convolution Neural Network for training and recognition of characters.
CNN is trained on MNIST dataset to detect digits.

## Getting Started

How to use
```    
git clone https://github.com/YannyTwoo/sudoku-solver.git
cd SolveSudoku
python3 sudoku.py <path/to/input_image>
```
 
## Prerequisites

- Python 3.5
- OpenCV
```
sudo apt-get install python-opencv
```
## Procedure
 > 1. Image preprocessing (Thresholding).
 > 2. Find the largest contour (sudoku square).
 > 3. Get the cordinates of **largest contour**.
 > 4. Crop the image.
 > 5. Perform **Warp perspective** on image
 > 5. Extract each cells from the image by slicing the sudoku grid.
 > 6. Extract the **largest component** in the sudoku image (number).
 > 7. Remove noise in block.
 > 8. Send the number to pre trained Digit Recogition model.
 > 9. Send the grid to Sudoku Solver to perform the final step.
## Working 

#### Input image of Sudoku-
![Input image of sudoku](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/sudoku.jpg)

#### Image of Sudoku after thresholding-
![Threshold image of sudoku](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/threshold.jpg)

#### Contour corners of Sudoku-
![Contour of sudoku](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/contour.jpg)

#### Warp Image-
![Warp of sudoku](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/warp.jpg)

#### Final output of ExtractSudoku-
![Final image of sudoku](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/final.jpg)


#### Extracted grid-
![extracted grid](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/extracted_grid.png)

#### Solved grid-
![Solved grid](https://github.com/YannyTwoo/sudoku-solver/blob/master/images/solved_grid.png)



