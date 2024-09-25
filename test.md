# Test

## Test

### Test

#### Test

##### Test

###### Test

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

```python
# Function to calculate the area of a rectangle
def calculate_area(width, height):
    return width * height

# Main function to get user input and display the area
def main():
    try:
        # Get user input for width and height
        width = float(input("Enter the width of the rectangle: "))
        height = float(input("Enter the height of the rectangle: "))
        
        # Calculate the area
        area = calculate_area(width, height)
        
        # Display the result
        print(f"The area of the rectangle is: {area:.2f}")
    
    except ValueError:
        print("Error: Please enter valid numbers.")

# Ensure the main function runs only when the script is executed directly
if __name__ == "__main__":
    main()
```

- Item 1
- Item 2
- Item 3
    * Subitem 1
    * Subitem 2
    * Subitem 3
- Item 4

1. Item 1
2. Item 2
3. Item 3
    * Subitem 1
    * Subitem 2
    * Subitem 3
4. Item 4

> This is a blockquote.

**Bold text**

*Italic text*

~~Strikethrough text~~

[Link to Google](https://www.google.com)

![Image](https://via.placeholder.com/150)

![Large image](https://via.placeholder.com/1000)


| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
| Cell 7   | Cell 8   | Cell 9   |

---

***

```
This is a code block
```