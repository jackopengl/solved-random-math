Download Link: https://assignmentchef.com/product/solved-random-math
<br>
Requirements Document

<table style="height: 1002px;" width="950">

 <tbody>

  <tr>

   <td width="157"><strong>Application Title:</strong></td>

   <td width="481">Random Math</td>

  </tr>

  <tr>

   <td width="157"><strong>Purpose:</strong></td>

   <td width="481">The Math Lab program allows the user to have randomly created math problems presented to them with immediate feedback concerning their answer and results saved to a file.</td>

  </tr>

  <tr>

   <td width="157"><strong>Program Procedures:</strong></td>

   <td width="481">The user may choose the type of math problem to create (+, -, *, /) as well as a maximum and a minimum number to use in the development of the problems.  A problem will be created and displayed.  The user will answer the problem and feedback will be given concerning the answer.  All problems, correct answers, and submitted answers will be saved to a txt file.</td>

  </tr>

  <tr>

   <td width="157"><strong>Algorithms, Processing, and Conditions:</strong></td>

   <td width="481">1.        The user must be able to choose the maximum number to use in creation of the problem.2.       The user must be able to choose the minimum number to use in creation of the problem.3.       The user must be able to choose the type of operator to use in the problem.4.       The user must be provided with a button to produce a randomly generated math problem based on the previous conditions.5.       The user must be able to enter an answer to the problem.6.       The program must provide feedback for the user concerning the problem, submitted answer, and correct answer.7.       The program must save the problem, submitted answer, and correct answer to a file for tracking.8.       The user should be provided with a button to clear the answer and problem.</td>

  </tr>

  <tr>

   <td width="157"><strong>Notes and Restrictions:</strong></td>

   <td width="481">1.        Any results (entered or actual from program) should be rounded to two decimal places (if needed).</td>

  </tr>

  <tr>

   <td width="157"><strong>Comments:</strong></td>

   <td width="481">1.        A graphic depicting mathematics (mathpic.bmp) should be used in the program.</td>

  </tr>

 </tbody>

</table>




Event Planning Document

<table style="height: 4275px;" width="934">

 <tbody>

  <tr>

   <td width="133"><strong>Program Name:</strong>Random Math</td>

   <td width="84"><strong>Developer:</strong>You!</td>

   <td width="238"><strong>Object:</strong>frmRandomMath</td>

   <td width="183">  </td>

  </tr>

  <tr>

   <td width="133"><strong>Object</strong></td>

   <td width="84"><strong>Event Trigger</strong></td>

   <td colspan="2" width="421"><strong>Event Processing</strong></td>

  </tr>

  <tr>

   <td width="133">frmRandomMath</td>

   <td width="84">Load</td>

   <td colspan="2" width="421">Clear the lblToWork label’s text. Clear the txtAnswer textbox’s text. Set the focus to the txtLargestNum textbox. The layout of the form should be:</td>

  </tr>

  <tr>

   <td width="133">btnCreateProblem</td>

   <td width="84">Click</td>

   <td colspan="2" width="421">Clear txtAnswer textbox’s text. Clear lblAnswerHere label’s text. Check that a smallest number was entered in txtSmallestNum and is an integer. Check that a largest number was entered in txtLargestNum and is an integer. Check that largest number is larger than smallest number. Check that an operator was selected from the combobox cboOperator. Provide feedback to the user in the form of a message box for any errors on the previous if needed (catch format, overflow, system exceptions). If there are no problems with the numbers or the selected operator, call to one of the following sub procedures (based on selected operator):1.        AdditionProblem()2.       SubtractionProblem()3.       MultiplicationProblem()4.       DivisionProblem() Set focus to txtAnswer text box. </td>

  </tr>

  <tr>

   <td width="133">btnSubmit</td>

   <td width="84">Click</td>

   <td colspan="2" width="421">Check that an answer was provided in the txtAnswer text box. Check that the entry is a valid number (may be integer or decimal). Provide feedback to the user in the form of a message box for errors on the previous if needed (catch format, overflow, system exceptions). Compare the actual answer (rounded to 2 decimal places) to the submitted answer (rounded to 2 decimal places).EX:  Decimal.Round(decDecTypeVariable, 2) If correct display a message box with the problem and answers in the format as follows: If incorrect, display a message box with the problem and answer in the format as follows: Write the problem, correct answer, and submitted answer to a comma delimited txt file (StudentMathResults.txt) in the following format (from previous two screenshot examples):8 + 7,Correct Answer = 15,Submitted Answer = 1510 + 4,Correct Answer = 14,Submitted Answer = 13 Any errors when opening the file should be handled with a message box and closing of the program. Clear the variables related to the answer, the submitted answer, clear the label lblToWork, clear the textbox txtAnswer, set the focus to btnCreateProblem button.</td>

  </tr>

  <tr>

   <td width="133">btnClear</td>

   <td width="84">Click</td>

   <td colspan="2" width="421">Clear lblToWork label’s text. Clear txtAnswer textbox’s text. Set focus to btnCreateProblem button.</td>

  </tr>

  <tr>

   <td width="133">AdditionProblem()</td>

   <td width="84">Sub procedure call</td>

   <td colspan="2" width="421">Retrieve two random numbers through two separate calls to CreateANumber(). Create the addition problem and display it in lblToWork Calculate and store the answer to the problem.</td>

  </tr>

  <tr>

   <td width="133">SubtractionProblem()</td>

   <td width="84">Sub procedure call</td>

   <td colspan="2" width="421">Retrieve two random numbers through two separate calls to CreateANumber(). Create the subtraction problem and display it in lblToWorkNOTE:  Prior to creating the problem, the numbers should be compared so that the smaller is subtracted from the larger. Calculate and store the answer to the problem.</td>

  </tr>

  <tr>

   <td width="133">MultiplicationProblem()</td>

   <td width="84">Sub procedure call</td>

   <td colspan="2" width="421">Retrieve two random numbers through two separate calls to CreateANumber(). Create the multiplication problem and display it in lblToWork Calculate and store the answer to the problem.</td>

  </tr>

  <tr>

   <td width="133">DivisionProblem()</td>

   <td width="84">Sub procedure call</td>

   <td colspan="2" width="421">Retrieve two random numbers through two separate calls to CreateANumber(). Create the division problem and display it in lblToWorkNOTE:  Prior to creating the problem, the numbers should be compared so that the smaller is divided into the larger. Calculate and store the answer to the problem.</td>

  </tr>

  <tr>

   <td width="133">CreateANumber()</td>

   <td width="84">Function procedure call</td>

   <td colspan="2" width="421">Initialize the random number generator. Call to the random number generator using the bounds of the min and max numbers to create a random number. Return an integer value to the calling procedures. To simplify this, the following procedure should work for you if you have the class level variables _intMaxNum and _intMinNum: </td>

  </tr>

 </tbody>

</table>




Use Case Definition

<ol>

 <li>The Windows application opens with a text box where the user can enter the maximum number (integer) to use in the generation of numbers for use in the problem.</li>

 <li>The Windows application opens with a text box where the user can enter the minimum number (integer) to use in the generation of numbers for use in the problem.</li>

 <li>The Windows application opens with a combo box where the user can choose the operator for use in the problem.</li>

 <li>The user clicks the Create Problem button.</li>

 <li>The program displays the mathematics problem using two randomly generated integers and the operator selected by the user.</li>

 <li>The focus is moved to the answer text box and the user types in the answer.</li>

 <li>The user clicks the Submit Answer button.</li>

 <li>The user is presented with a message box displaying correct/incorrect, the problem, the correct answer, and the submitted answer. The user must acknowledge the message box before returning to the program.</li>

 <li>The problem, the correct answer, and the submitted answer are written to a txt file.</li>

 <li>Problem and answer are cleared on acknowledgement of the message box and the focus is returned to the Create Problem button.</li>

</ol>


