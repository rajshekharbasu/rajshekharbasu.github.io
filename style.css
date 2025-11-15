// Update current time in header
function updateTime() {
    const now = new Date();
    const timeString = now.toLocaleTimeString('en-US', {
        hour: 'numeric',
        minute: '2-digit',
        second: '2-digit',
        hour12: true
    });
    const timeElement = document.getElementById('current-time');
    if (timeElement) {
        timeElement.textContent = timeString;
    }
}

// Update time every second
setInterval(updateTime, 1000);
updateTime(); // Initial call

// Smooth scrolling for anchor links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// Add active state to navigation
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('nav a[href^="#"]');

function highlightNavigation() {
    const scrollPosition = window.scrollY + 100;

    sections.forEach(section => {
        const sectionTop = section.offsetTop;
        const sectionHeight = section.offsetHeight;
        const sectionId = section.getAttribute('id');

        if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
            navLinks.forEach(link => {
                link.style.borderBottom = '2px solid transparent';
                if (link.getAttribute('href') === `#${sectionId}`) {
                    link.style.borderBottom = '2px solid #000';
                }
            });
        }
    });
}

window.addEventListener('scroll', highlightNavigation);
highlightNavigation(); // Initial call

// Hover effects for project rows
const projectRows = document.querySelectorAll('.section-row');
projectRows.forEach(row => {
    row.addEventListener('mouseenter', function() {
        this.style.transition = 'background-color 0.2s ease';
    });
});

// Add fade-in animation on page load
document.addEventListener('DOMContentLoaded', function() {
    console.log('Portfolio loaded successfully');
    
    // Subtle fade-in effect
    document.body.style.opacity = '0';
    setTimeout(() => {
        document.body.style.transition = 'opacity 0.5s ease';
        document.body.style.opacity = '1';
    }, 100);

    // Animate face placeholders (optional - for when you add real images)
    const faces = document.querySelectorAll('.face-placeholder');
    faces.forEach((face, index) => {
        face.style.opacity = '0';
        setTimeout(() => {
            face.style.transition = 'opacity 0.5s ease';
            face.style.opacity = '1';
        }, 200 * index);
    });
});

// Sticky header with hide/show on scroll
let lastScroll = 0;
const header = document.querySelector('header');

window.addEventListener('scroll', () => {
    const currentScroll = window.pageYOffset;
    
    if (currentScroll > lastScroll && currentScroll > 100) {
        header.style.transform = 'translateY(-100%)';
        header.style.transition = 'transform 0.3s ease';
    } else {
        header.style.transform = 'translateY(0)';
    }
    
    lastScroll = currentScroll;
});

// Optional: Add intersection observer for lazy loading images
const imageObserver = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            const img = entry.target;
            // Add your image loading logic here when you upload images
            observer.unobserve(img);
        }
    });
}, {
    rootMargin: '50px'
});

// Observe all image placeholders
document.querySelectorAll('.image-placeholder').forEach(img => {
    imageObserver.observe(img);
});
