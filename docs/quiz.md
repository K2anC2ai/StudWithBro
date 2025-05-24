# Quiz

<div id="quiz-app" class="quiz-container">
  <div class="quiz-question">
    <div class="quiz-qnum">1</div>
    <div>
      <div class="quiz-qtext"><b>What is 2 + 2?</b></div>
      <div class="quiz-choices">
        <label class="quiz-choice"><input type="radio" name="q1" value="3"> 3</label>
        <label class="quiz-choice"><input type="radio" name="q1" value="4"> 4</label>
        <label class="quiz-choice"><input type="radio" name="q1" value="5"> 5</label>
      </div>
    </div>
  </div>
  <div class="quiz-question">
    <div class="quiz-qnum">2</div>
    <div>
      <div class="quiz-qtext"><b>What is the capital of France?</b></div>
      <div class="quiz-choices">
        <label class="quiz-choice"><input type="radio" name="q2" value="London"> London</label>
        <label class="quiz-choice"><input type="radio" name="q2" value="Paris"> Paris</label>
        <label class="quiz-choice"><input type="radio" name="q2" value="Berlin"> Berlin</label>
      </div>
    </div>
  </div>
  
  <button id="quiz-submit" class="quiz-btn">Submit</button>
  <div id="quiz-result" class="quiz-result"></div>
</div>

<script>
document.getElementById('quiz-submit').addEventListener('click', function() {
  let score = 0;
  if (document.querySelector('input[name="q1"]:checked')?.value === "4") score++;
  if (document.querySelector('input[name="q2"]:checked')?.value === "Paris") score++;
  document.getElementById('quiz-result').innerHTML = "Your score: " + score + "/2";
  // Update sidebar score
  const examScore = document.getElementById('exam-score');
  if (examScore) examScore.innerText = score + "/2";
});
</script>