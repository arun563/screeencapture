# screeencapture
Javascript library and code to handle the screenshot feature

# Use following js code

html2canvas(document.body,{background: '#fff'}).then(function(canvas) {	
          // append the image canvas on document body
	        document.body.appendChild(canvas);	
	        // Get base64URL
	        var base64URL = canvas.toDataURL('image/jpeg').replace('image/jpeg', 'image/octet-stream');
 });

# Save file to a folder locally or remotely
// AJAX request
$.ajax({
	           url: '../includes/clsajax.php',
	           type: 'post',
	           data: {type: 'saveshapeshot', folder: 'foldername', image: base64URL},
	           success: function(data){
	              console.log('Upload successfully');
	              $('body').find('canvas').remove();
	           }
});


# Function Call
<button type="submit" class="ss-ml-0 ss-bg-green ss-ptb-10 ss-plr-20" onclick="screenshot();">Click to Capture </button>

That's all!
Have fun!!!
