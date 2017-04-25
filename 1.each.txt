/*  each
     --> With Arrays

     for(String s1:names){ SOP(s1())}
*/

var names=['Praveen','james','Amber','Ruth','Bucky'];

_.each(names,function(name,idx){
    //console.log(name+' is at index '+idx+' and size is '+list.length);
    console.log(name);
});      

//--> Object Data

 var persons={name:'Praveen',age:45,addr:'Chennai'};

 _.each(persons,function(value,key){
   console.log(value+' is at '+key);
  
    // console.log(list);
});


var persons=[
{
    name:'Praveen',
    age:20
},
{
    name:'James',
    age:40
},
{
    name:'Ruth',
    age:76
},

];

_.each(persons,function(person,idx){
    console.log(person.name+" is "+person.age+' years old '+ 'at index '+idx);
});

//Array (context)

var step4=function(){
    var people={
      names:['Praveen','Ravi','Kumar','Ramu','Kavya'],
      getMessage:function(name){
          return 'Hello there '+name;
      } // end of function
    }; // end of people obj

    _.each(people.names,function(element,idx,list){
           console.log(this.getMessage(element));
    },people); 
} // end of main fun

//Object (context)

var step5=function(){
var author={
    firstName:'Praveen',
    lastName:'Reddy'
},
messager={
    getGreeting:function(){
        return 'Hello!';
    },
    getMessage:function(msg){
        return this.getGreeting()+ msg;
    }
}; // end of messenger

_.each(author,function(value,key){
    console.log(this.getMessage(value));
},messager);

}// end of step5 fun






