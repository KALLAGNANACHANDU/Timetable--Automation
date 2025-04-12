# Timetable--Automation

1. Data Structures:

courses: A dictionary storing course information, including faculty and required slots.
rooms: A list of available rooms.
time_slots: A list of available time slots.
faculty_availability: A dictionary storing faculty availability for different time slots.
timetable: A dictionary to store the final timetable.
2. Timetable Class:

__init__: Initializes the Timetable object with the provided data.
is_valid: Checks if assigning a course to a room and time slot is valid, considering faculty availability, room availability, and faculty teaching load.
assign: Tries to assign a course to a room and time slot if it's valid.
generate_timetable: Iterates through courses and attempts to assign them to suitable slots. If successful, it returns True; otherwise, False.
3. Main Execution:

Creates a Timetable object with the provided data.
Calls generate_timetable to create the timetable.
Prints the timetable if successful; otherwise, prints an error message.
4. Logic:

The code uses a backtracking approach. It tries to assign a course to a slot, and if it's valid, it moves to the next course.
If it encounters a conflict (e.g., room or faculty unavailable), it backtracks and tries a different slot.
This process continues until all courses are assigned or it determines that a valid timetable cannot be created.
