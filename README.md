# BMI-Calculator-using-React
## AIM:
To create a BMI calculator using react js.

## SOFTWARE:
Visual Studio Code

## ALGORITHM
Create a new project using Create React App or your preferred method. Set up the necessary dependencies.
In your components directory, create a new file called "BMICalculator.js". Import the necessary React dependencies.
Define the BMICalculator component
Open your App.js file.Import the BMICalculator component
Use the BMICalculator component in the main App component
Run your React.js development server to see the BMI calculator in action.
## PROGRAM:
~~~
java

import React, { useState } from 'react';

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBMI] = useState(null);

  const calculateBMI = () => {
    const heightInMeters = height / 100;    
    const bmiValue = weight / (heightInMeters * heightInMeters);
    setBMI(bmiValue.toFixed(2));
  };

  return (
    <div>
      <h2>BMI Calculator</h2>
      <div>
        <label htmlFor="weight">Weight (kg):</label>
        <input
          type="text"
          id="weight"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
        />
      </div>
      <div>
        <label htmlFor="height">Height (cm):</label>
        <input
          type="text"
          id="height"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
        />
      </div>
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <p>Your BMI is: {bmi}</p>}
    </div>
  );
}
export default BMICalculator;
~~~
## OUTPUT:
![image](https://github.com/SdMdZahi7/BMI-Calculator-using-React/assets/94187572/4a9b4739-6c33-4a32-b88c-491ffb9ba0be)

### After the calculation:
![image](https://github.com/SdMdZahi7/BMI-Calculator-using-React/assets/94187572/3bf149b9-5cb3-4675-949e-086116280d00)

## RESULT:
Thus the BMI calculator is created.

