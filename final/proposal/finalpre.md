-i finished all of the page using bootstap and add javascript function to pages 'relationship' and 'what pony r u' and i also rebuilt homepage 

code snippet
there are 3 screen shot of my code in this file
 --1 how i figured out how to strech the img to fit the whole background so there's no werid gao on top and bottom of the page
 --2 using javascript and varaibles to change the content in the pop-up window and not having to rewrite the content for every possible result
 --3 finally figured out using javascript to do the pop-up window instead of just displaying an additional div at bottom of the page
 --4 this is the part where i change the backgorund color of the popup window based on the character using javascript and using array
 
 const characterColors = {
    "PINKY PIE": "#FFC0CB", 
    "APPLEJACK": "#DEB887", 
    "RARITY": "#DDA0DD", 
    "TWILIGHT SPARKLE": "#9370DB", 
    "FLUTTERSHY": "#FADADD", 
    "RAINBOW DASH": "#1E90FF" 
};

...the part in screenshot 2...

        modalContent.style.backgroundColor = characterColors[character]; 
        modalBody.innerHTML = resultHtml;

        var resultModal = new bootstrap.Modal(document.getElementById('resultModal'));
        resultModal.show();
    });

    tryAgainButton.addEventListener('click', function() {
        var resultModal = bootstrap.Modal.getInstance(document.getElementById('resultModal'));
        resultModal.hide();
        form.reset();
        modalContent.style.backgroundColor = ''; 
    });
});
