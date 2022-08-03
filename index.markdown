<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Example 3a&quot;)\n" +
    "      \n" +
    "weekendRate = False\n" +
    "day = input(&quot;Enter the day of the week: &quot;)\n" +
    "if day == &quot;Saturday&quot; or day == &quot;Sunday&quot;:\n" +
    "    weekendRate = True\n" +
    "print(&quot;WeekendRate&quot;,weekendRate)\n" +
    "print (&quot;\nExample 3b: day = Sunday&quot;)\n" +
    "weekendRate = False\n" +
    "day = &quot;Sunday&quot;\n" +
    "if (not day == &quot;Saturday&quot;) and (not day == &quot;Sunday&quot;):\n" +
    "    weekendRate = False\n" +
    "print(&quot;WeekendRate&quot;,weekendRate)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
