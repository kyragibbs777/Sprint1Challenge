# Sprint1Challenge
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Web Sprint 1 Challenge</title>
  <style>
    .widget {
      padding: 0 0 0.5rem 0.65rem;
      margin-bottom: 0.5rem;
      border: 1px solid black;
      border-radius: 0.5rem;
    }

    .widget p {
      font-size: 0.75rem;
      font-style: italic;
    }
  </style>
</head>

<body>
  <h1>Web Sprint 1 Challenge </h1>
  <p>❗ See the script tag for instructions on completing your Challenge</p>
  <!-- widgets start -->
  <section class="widget">
    <p>This widget uses the advancedBatteryCare function</p>
    <input type="range" min="0" max="100" value="50" id="sliderBattery"> 
    <div id="infoBattery">your battery is at 50%</div>
  </section>
  <!-- widgets end -->

  <script id="challenge">
    // In CHALLENGES 1-4 you will write JavaScript functions.
    // In CHALLENGE 5 you will edit the HTML to add some missing id attributes.

    // ❗ Each function is already scaffolded for you. You will need to fill in each function's parameters and body.
    // ❗ Do not rename the functions provided, and do not create any other script tags.
    // ❗ As you go through each challenge, load this file in the browser and debug using the Console.
    // ❗ All challenges that returns strings must return the EXACT string given in the instructions to pass.

    // 👉 CHALLENGE 1
    function concatenator(a,b) {
      // 🧠 concatenator takes two arguments named a and b:
      //    * If a and b are strings, return them concatenated
      //    * If a and b are numbers, return their sum
      // 💡 Other conditions that must be met:
      //    * Both a and b must be of the same type. If they are not the same type, return the string "a and b must be of the same type"
      //    * a and b can be either numbers or strings. If they are not, return "a and b must be numbers or strings"
      // ❗ Hint: The order of the conditions in the pseudo-code above and in the actual code is not necessarily the same
      // ❗ Hint: It's advised to deal with the other conditions first, like arguments being of the wrong type.
      //          In the real world, these are considered "edge cases"
             
      if (typeof a !== typeof b){
        return 'a and b must be of the same type'
      }
      
      if (typeof a !== 'string' && typeof a !== 'number' ){
        return 'a and b must be numbers or strings'}

        return a + b
       }
      

    // 👉 CHALLENGE 2
    function falsinessDetector(a,b,c,d,e) {
      // 🧠 falsinessDetector takes five arguments named a, b, c, d, and e which are values of any type:
      //    * If some values are truthy and some falsy, return the string "some values truthy and some falsy"
      //    * If all values are falsy, return the string "all values falsy"
      //    * If all values are truthy, return the string "all values truthy"
      
     
      if (a || b || c || d || e) {
        
        if (!a || !b || !c || !d || !e) {
            return "some values truthy and some falsy";
        } else {
            return "all values truthy";
        }
    } else {
        return "all values falsy";
    }


  
    }

    // 👉 CHALLENGE 3
    function triangleAnalyzer(angleA, angleB, angleC) {
      // 🧠 triangleAnalyzer takes three arguments named angleA, angleB, and angleC:
      //    * If any angle is 90 degrees, return the string "this is a right triangle"
      //    * If any angle is over 90 degrees, return the string "this is an obtuse triangle"
      //    * If all angles are under 90 degrees, return the string "this is an acute triangle"
      // 💡 Other conditions that must be met:
      //    * All angles must be of type number. If not, return the string "all angles must be numbers"
      //    * All angles must be greater than zero. If not, return the string "all angles must be greater than zero"
      //    * The three angles must add up to 180. If not, return the string "angles must total 180"
      // ❗ Hint: the order of the conditions in the pseudo-code above and in the actual code is not necessarily the same
      // ❗ Hint: It's advised to deal with the other conditions first, like arguments being of the wrong type.
      //          In the real world, these are considered "edge cases".
      if (typeof angleA !== 'number' || typeof angleB !== 'number' || typeof angleC !== 'number') {
        return "all angles must be numbers";
    }

    if (angleA <= 0 || angleB <= 0 || angleC <= 0) {
        return "all angles must be greater than zero";
    }

    const totalAngles = angleA + angleB + angleC;
    if (totalAngles !== 180) {
        return "angles must total 180";
    }

    if (angleA === 90 || angleB === 90 || angleC === 90) {
        return "this is a right triangle";
    }

    if (angleA > 90 || angleB > 90 || angleC > 90) {
        return "this is an obtuse triangle";
    }

    return "this is an acute triangle";
      
    }

    // 👉 CHALLENGE 4
    function advancedBatteryCare(percentage) {
      // 🧠 advancedBatteryCare takes an argument named percentage that will be a number between 0 and 100 inclusive:
      //    * If percentage in the range between 20 and 80 inclusive (E.G. 47), return a string like "your battery is at 47%"
      //    * If percentage over 80, return the string "please unplug charger"
      //    * If percentage under 20, return the string "please connect charger"
      //    * If percentage exactly 0, return the string "congrats, battery dead"
      //    * If percentage exactly 100, return the string "congrats, you cooked your battery"

      if (typeof percentage !== 'number' || percentage < 0 || percentage > 100) {
        return "percentage must be a number between 0 and 100 inclusive";
    }

    if (percentage >= 20 && percentage <= 80) {
        return `your battery is at ${percentage}%`;
    } else if (percentage === 100) {
        return "congrats, you cooked your battery";
    } else if (percentage === 0){
        return "congrats, battery dead"
    } else if (percentage < 20){
        return "please connect charger"
    }
      else if (percentage > 80) {
        return "please unplug charger";
    }
}
    
    // 👉 CHALLENGE 5
    // 🧠 The advancedBatteryCare function implemented above is being used to display a widget on the web page
    // However, some HTML elements are missing an id attribute that would allow the JavaScript code to find them
    // Visit the following website: `https://bloominstituteoftechnology.github.io/W_U1_S1_sprint_challenge_v2/`
    //    * Interact with the site to see the widget in action
    //    * Use Chrome Dev Tools/Elements tab to find the missing ids
    //    * Add the missing ids to the corresponding HTML elements in this document and make the widget work
  

    // 🧪 TESTS, do not make any changes below this line ===================
    // 🧪 TESTS, do not make any changes below this line ===================
    // 🧪 TESTS, do not make any changes below this line ===================
    globalThis.challengeVersion = 2
    globalThis.concatenator = concatenator
    globalThis.falsinessDetector = falsinessDetector
    globalThis.triangleAnalyzer = triangleAnalyzer
    globalThis.advancedBatteryCare = advancedBatteryCare

    if (typeof module === 'undefined') {
      try {
        runTests('CHALLENGE 1 - concatenator', concatenator, [
          [[1, 'a'], 'a and b must be of the same type'],
          [['a', 1], 'a and b must be of the same type'],
          [[true, false], 'a and b must be numbers or strings'],
          [[null, null], 'a and b must be numbers or strings'],
          [['toyota', ' camry'], 'toyota camry'],
          [[3, 5], 8],
          [[3, -5], -2],
        ])
        runTests('CHALLENGE 2 - falsinessDetector', falsinessDetector, [
          [[1, '2', true, '0', ' '], 'all values truthy'],
          [[-1, '2', !false, '0', '-0'], 'all values truthy'],
          [[0, -0, false, '', false], 'all values falsy'],
          [[2 - 2, -0, !true, '' + '', !!false], 'all values falsy'],
          [[0, -0, false, '', ' '], 'some values truthy and some falsy'],
          [[5, -0, !true, ' ', '0'], 'some values truthy and some falsy'],
        ])
        runTests('CHALLENGE 3 - triangleAnalyzer', triangleAnalyzer, [
          [[], 'all angles must be numbers'],
          [['90', '60', '30'], 'all angles must be numbers'],
          [[90, 60, '30'], 'all angles must be numbers'],
          [[0, 0, 180], 'all angles must be greater than zero'],
          [[-180, 180, 180], 'all angles must be greater than zero'],
          [[90, 60, 31], 'angles must total 180'],
          [[90, 60, 29], 'angles must total 180'],
          [[90, 60, 30], 'this is a right triangle'],
          [[45, 45, 90], 'this is a right triangle'],
          [[35, 90, 55], 'this is a right triangle'],
          [[91, 60, 29], 'this is an obtuse triangle'],
          [[40, 45, 95], 'this is an obtuse triangle'],
          [[25, 100, 55], 'this is an obtuse triangle'],
          [[60, 60, 60], 'this is an acute triangle'],
        ])
        runTests('CHALLENGE 4 - advancedBatteryCare', advancedBatteryCare, [
          [[0], 'congrats, battery dead'],
          [[100], 'congrats, you cooked your battery'],
          [[19], 'please connect charger'],
          [[81], 'please unplug charger'],
          [[20], 'your battery is at 20%'],
          [[50], 'your battery is at 50%'],
          [[80], 'your battery is at 80%'],
        ])
        console.log('\nCHALLENGE 5 does not have auto tests')
        function runTests(testName, func, tests) {
          let results = []
          tests.forEach(test => {
            const argsList = test[0]
            const expected = JSON.stringify(test[1])
            const actual = JSON.stringify(func.apply(null, argsList))
            results.push([argsList, expected, actual])
          })
          console.log('\n' + testName)
          if (results.every(result => result[1] === result[2])) console.log('\t✅ All tests pass')
          else if (results.every(result => result[1] !== result[2])) console.log('\t❌ All tests fail')
          else results.forEach((result, idx) => {
            if (result[1] === result[2]) console.log(`\t✅ Test ${idx + 1} passes`)
            else console.log(`\t❌ Test ${idx + 1} fails: ${func.name}(${result[0]
              .map(JSON.stringify)}) should return ${result[1]} but returns ${result[2]}`)
          })
        }
        try {
          sliderBattery.onchange = () => {
            infoBattery.textContent = advancedBatteryCare(Number(sliderBattery.value))
          }
        } catch { }
      } catch (err) { console.error(err.stack) }
    }
  </script>
</body>

</html>
