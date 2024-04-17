var main = function() {
    var muted = false;
    var volume = 1; // Initial volume set to maximum
  
    // Play button
    $('#play').click(function(){
        $('#message').text("Playing track");
        $('#player').trigger("play");
    });
  
    // Pause button
    $('#pause').click(function(){
        console.log("Pause button clicked"); // Check if the event listener is triggered
        $('#message').text("Track paused");
        $('#player').trigger("pause");
    });
   
    // Mute button
    $('#mute').click(function(){
        muted = !muted; // Toggle the muted variable
        $('#player').prop('muted', muted); // Set the muted property of the player
        
        // Update message based on mute status
        if (muted) {
            $('#message').text("Track muted");
        } else {
            $('#message').text("Track unmuted");
        }
    });
    
    // Unmute button
    $('#unmute').click(function(){
        muted = false; // Set muted to false to unmute
        $('#player').prop('muted', muted); // Set the muted property of the player
        
        // Update message
        $('#message').text("Track unmuted");
    });
    
    // Stop button
    $('#stop').click(function(){
        $('#message').text("Track stopped");
        $('#player').trigger("pause"); // Pause the music
        $('#player').prop('currentTime', 0); // Set the currentTime of the track to 0
    });
    
    // Volume Up button
    $('#volumeUp').click(function(){
        if (volume < 1) {
            volume += 0.1; // Increase volume by 0.1
            $('#player').prop('volume', volume); // Set the volume property of the player
            $('#message').text("Volume up: " + Math.round(volume * 10) / 10); // Update message
        }
    });
    
    // Volume Down button
    $('#volumeDown').click(function(){
        if (volume > 0) {
            volume -= 0.1; // Decrease volume by 0.1
            $('#player').prop('volume', volume); // Set the volume property of the player
            $('#message').text("Volume down: " + Math.round(volume * 10) / 10); // Update message
        }
    });
}; 

$(document).ready(main); 