def calculate_percentage(marks_obtained, total_marks):
    """
    Calculate the percentage of marks obtained out of total marks.

    Parameters:
    marks_obtained (float): The marks obtained by the student.
    total_marks (float): The total marks possible.

    Returns:
    float: The percentage of marks obtained.
    """
    if total_marks == 0:
        raise ValueError("Total marks cannot be zero.")
    
    percentage = (marks_obtained / total_marks) * 100
    return percentage

def main():
    try:
        marks_obtained = float(input("Enter the marks obtained: "))
        total_marks = float(input("Enter the total marks: "))
        
        percentage = calculate_percentage(marks_obtained, total_marks)
        print(f"The percentage of marks obtained is {percentage:.2f}%.")
    
    except ValueError as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()
