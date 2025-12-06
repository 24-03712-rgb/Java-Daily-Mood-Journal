Daily Mood Journal


<img width="700" height="400" alt="6c1ea653-6ac8-4958-b451-1c39d5683183" src="https://github.com/user-attachments/assets/4c47f33d-9fee-4b49-bc74-11da8a6cadd7" />

The Daily Mood Journal is a simple, interactive, and console-based mental health tool designed to help users track their daily emotional state. It allows users to record their mood, write a short note about their day, and receive personalized feedback based on the mood they enter. Each entry is organized by date, making it easy for users to review past logs at any time. By providing a structured way to document emotions and daily reflections, the program promotes self-awareness, emotional well-being, and the identification of personal mood patterns. Through consistent journaling, users can better understand their mental state, manage stress, and develop healthier coping habits over time.

OOP Concepts Applied

This project applies the four core principles of Object-Oriented Programming: Abstraction, Encapsulation, Inheritance, and Polymorphism.

> Abstraction is used by creating an abstract class JournalEntry, which represents the general idea of any journal record. This class contains shared properties (date, note) and an abstract method displayEntry() that forces all subclasses to define their own display behavior. This hides unnecessary details and provides a clean, simplified view of journal entries.


> Encapsulation is applied through the use of private fields and public getters/setters in both JournalEntry and MoodEntry. For example, note, date, and mood cannot be accessed directly from outside the class. Instead, they can only be accessed or modified through methods like getNote(), setNote(), and getMood(). This protects the data and enforces controlled access.


> Inheritance is shown when the class MoodEntry extends JournalEntry. MoodEntry inherits all fields and behaviors from the abstract parent class, such as date, note, and the abstract method displayEntry(). It adds additional behavior by including the mood field and specific methods related to mood tracking.


> Polymorphism is evident when the program uses the same method name but executes different behavior. The displayEntry() method is overridden in MoodEntry, giving it a customized output. When viewing all entries in the JournalManager class, each object is handled through a JournalEntry reference, allowing the program to call the correct version of displayEntry() depending on the actual object type. This demonstrates runtime (dynamic) polymorphism.


Program Structure

Main Class Overview

		Entry point of the program.
		
		Handles menu display, user input, and directs actions to JournalManager.

Class Descriptions
		JournalEntry (Abstract Class)
		
		Represents a general journal entry.
		
		Fields: LocalDate date, String note

Methods:
		getDate(), getNote(), setNote()
		
		displayEntry() → abstract method to be implemented by subclasses.
		
		Purpose: Base structure for all possible journal entry types.

MoodEntry (Subclass of JournalEntry)

		Specialized journal entry containing mood data.
		Additional field: String mood
		Overrides displayEntry() → adds mood + feedback from MoodAnalyzer.
		Purpose: Stores the user's mood and journal note for the day.

MoodAnalyzer
	
		A utility class that provides feedback depending on user's mood.
		Contains:
			Static method getFeedback(String mood)
		Purpose: Centralized logic for interpreting mood.

JournalManager
	
		Stores and manages all journal entries.
		Fields:
		ArrayList<JournalEntry> entries
		Scanner scanner
		Methods:
		addEntry() → creates a new MoodEntry and saves it
		viewEntries() → displays all entries (uses polymorphism)
		Purpose: Controls data management, processing, and user interactions.

How to run the program

Follow the steps below to compile and run the Daily Mood Journal program.

Go to Programiz Java Online Compiler. Open your browser and go to: https://www.programiz.com/java-programming/online-compiler/

Copy and paste your entire Java code. Paste your full Main.java code, including all classes in the same file.

Click the green run button at the top-right.

Use the input box. Your program requires user input, so Programiz will show an input field under the console when needed.

Continue interacting with your program. You can add entries, View entries, and Exit All through the same console area.

Sample Output
   
	Add New Entry


   <img width="700" height="200" alt="100" src="https://github.com/user-attachments/assets/cf5c00a0-f7d7-4deb-a5e5-33ac5f2f4679" />

  	View Past Entries


   <img width="700" height="200" alt="101" src="https://github.com/user-attachments/assets/434b0ff2-c981-4852-9be7-a286b8d9b757" />

    Invalid Choice


   <img width="700" height="200" alt="102" src="https://github.com/user-attachments/assets/e3c52668-7c14-4f68-b98e-373a58b1c3fc" />

    Exit


   <img width="700" height="200" alt="104" src="https://github.com/user-attachments/assets/e5599b20-fbe7-4fa4-81b0-18c04127350b" />



8.  Author and Acknowledgement
   Authors:

	Alim, Arlene D.


![575437619_852434590467027_8232135864407585414_n](https://github.com/user-attachments/assets/146c8bcd-3097-4769-91f1-26d8562a9cfd)

	
	Loterte, Samuel B.


![591202373_1929881794596503_6565027416893284165_n](https://github.com/user-attachments/assets/3d831fe9-2e54-4641-9264-a5f4c1d6e1f1)

	Pepillo, Angel A.


![3ba0053d-c596-4e3f-905a-b4446346c019](https://github.com/user-attachments/assets/669d5b98-3b50-4ffe-af75-307f545078c6)


We would like to thank everyone who helped us while working on this project. First, our instructor guided us and gave useful feedback that made the project easier to understand. A big thank you to our group members for supporting and helping each other throughout the project. We also want to thank online resources, especially Programiz, for providing examples and tools that helped us understand Java and apply Object-Oriented Programming concepts in our project. Without all the help we received, completing the Daily Mood Journal would have been much harder.


Future Enhancements 

Although the current version of the Daily Mood Journal is functional, several improvements can be added in future versions to enhance usability, flexibility, and overall user experience.

> Load Entries from a File - When the program starts, it can automatically read previously saved entries and display them. This will turn the program into a true long-term journal.

> Add More Mood Categories - Expand the list of mood options (e.g., Stressed, Excited, Tired, Motivated), allowing for more detailed tracking.

> Add Mood Statistics - Implement analytics such as the most common mood, mood trends per week, and average mood rating. These can help users better understand their emotional patterns.

> Edit or Delete Entries - Users may want to modify or remove older entries.
	
> Password Protection - Add a login system or password lock to keep the journal private and secure.

References 
https://www.programiz.com/java-programming/online-compiler/







