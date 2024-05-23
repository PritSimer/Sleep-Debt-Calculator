# Sleep-Debt-Calculator
switch // codecademy // beginners // practice
const getSleepHours = (day) => {

day = day.toLowerCase();

  switch (day) {
   case 'monday':
   return 6;
   case 'tuesday':
   return 7;
   case 'wednesday':
   return 8;
   case 'thursday':
   return 12;
   case 'friday':
   return 10;
   case 'saturday':
   return 12;
   case 'sunday':
   return 11;
  }
};

//console.log(getSleepHours('Sunday'));

const getActualSleepHours = () => {

return 8 + 7 + 8 + 6 + 8 + 3 + 8;

};
//console.log(getActualSleepHours());

const getIdealSleepHours = (idealHours) => {

return idealHours * 7;
}

//console.log(getIdealSleepHours(7.5));
//console.log(getActualSleepHours());

const calculateSleepDebt = ()=> {

let actualSleepHours = getActualSleepHours();

let idealSleepHours = getIdealSleepHours(7);

let sleepDebt = actualSleepHours - idealSleepHours;



if (actualSleepHours === idealSleepHours) {
  console.log('The user got the perfect amount of sleep and have '+sleepDebt+' sleep debt.');
} else if (actualSleepHours > idealSleepHours) {
  console.log('The user got more sleep than needed! They slept ' +sleepDebt+ ' hours more than needed!');
} else if (actualSleepHours < idealSleepHours){
  console.log('The user should get more rest. They lost out on '+ sleepDebt+ ' hours sleep!');
}
}

calculateSleepDebt();

