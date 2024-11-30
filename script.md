document.addEventListener('DOMContentLoaded', function() {
    // Add event listeners to the "View Details" buttons
    const buttons = document.querySelectorAll('.view-details-btn');
    
    buttons.forEach(button => {
        button.addEventListener('click', function() {
            alert('More details coming soon!');
        });
    });

    // Contact form validation
    const form = document.getElementById('contact-form');
    form.addEventListener('submit', function(e) {
        e.preventDefault();
        
        const name = form.querySelector('input[type="text"]').value;
        const email = form.querySelector('input[type="email"]').value;
        const message = form.querySelector('textarea').value;

        if (name && email && message) {
            alert('Thank you for your message! We will get back to you shortly.');
            form.reset();
        } else {
            alert('Please fill in all fields.');
        }
    });
});