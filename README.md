// Base class
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  introduce() {
    return `Hi, I'm ${this.name} and I'm ${this.age} years old.`;
  }
}

// Subclass Student
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this.grade = grade;
  }

  // Method overriding
  introduce() {
    return `Hi, I'm ${this.name}, a student in grade ${this.grade}.`;
  }

  study() {
    return `${this.name} is studying hard.`;
  }
}

// Subclass Teacher
class Teacher extends Person {
  constructor(name, age, subject) {
    super(name, age);
    this.subject = subject;
  }

  // Method overriding
  introduce() {
    return `Hello, I'm ${this.name}, a teacher of ${this.subject}.`;
  }

  teach() {
    return `${this.name} is teaching ${this.subject}.`;
  }
}

// Create objects
const student1 = new Student("Alice", 14, "8th");
const teacher1 = new Teacher("Mr. Smith", 40, "Mathematics");

// Use methods
console.log(student1.introduce()); // overridden version
console.log(student1.study());     
console.log(teacher1.introduce()); // overridden version
console.log(teacher1.teach());
