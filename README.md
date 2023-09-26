# app.js
oop
//Class
class User {
  _name ;
  #password ;

  constructor(name, password) {
    this._name = name;
    this.#password = password;
  }
  showDetail() {
    console.log(`ชื่อ ${this._name} , รหัสผ่าน ${this.#password}`);
  }
  set Name(newName) {
    this._name = newName;
  }
  set Password(newPassword) {
    this.#password = newPassword;
  }
  get Name() {
    return this._name;
  }
  get Password() {
    return this.#password;
  }
}
class Teacher extends User {
    #course
    constructor(name,password,course){
        super(name,password)
        this.#course=course
    }
    showDetail(){
        console.log(`ชื่อคุณครู ${this._name} สอนวิชา ${this.#course}`)
    }
}

class Student extends User{
    #score
    constructor(name,password,score){
        super(name,password)
        this.#score=score
    }
    showDetail(){
        console.log(`ชื่อนักเรียน ${this._name} สออบได้ ${this.#score}`)
    }
}

const user1=new Teacher("Milo",5647,"ภาษาไทย")
user1.showDetail()
const user2=new Teacher("Mono",5647,"ภาษาอังกฤษ")
user2.showDetail()
const user3 = new Student("Cocoa",7865,99)
user3.showDetail()
const user4 = new Student("Coki",7865,85)
user4.showDetail()
