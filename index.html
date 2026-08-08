// ============================================================
// MEDRISK CONSULTING - MASTER SCRIPT.JS
// Compiled from: index.html, about.html, service-detail.html, 
// booking.html, contact.html, pay.html
// ============================================================

document.addEventListener('DOMContentLoaded', function() {

    // ============================================================
    // 1. AUTO COPYRIGHT YEAR
    // ============================================================
    function updateCopyright() {
        const year = new Date().getFullYear();
        const yearElements = document.querySelectorAll('#year, #year2');
        yearElements.forEach(el => {
            if (el) el.textContent = year;
        });
    }
    updateCopyright();

    // ============================================================
    // 2. MOBILE HAMBURGER MENU
    // ============================================================
    function initMobileMenu() {
        const hamburger = document.getElementById('hamburger');
        const overlay = document.getElementById('mobileOverlay');

        if (hamburger && overlay) {
            hamburger.addEventListener('click', function() {
                overlay.classList.toggle('open');
                // Optional: change hamburger icon animation
                this.classList.toggle('active');
            });

            // Close menu when any link is clicked
            document.querySelectorAll('.mobile-overlay a').forEach(link => {
                link.addEventListener('click', function() {
                    overlay.classList.remove('open');
                    if (hamburger) hamburger.classList.remove('active');
                });
            });
        }
    }
    initMobileMenu();

    // ============================================================
    // 3. DROPDOWN TOGGLE (for mobile services dropdown)
    // ============================================================
    function initDropdownToggle() {
        const dropdownLabel = document.getElementById('mobileDropdownLabel');
        const subLinks = document.getElementById('mobileSubLinks');

        if (dropdownLabel && subLinks) {
            dropdownLabel.addEventListener('click', function(e) {
                e.preventDefault();
                this.classList.toggle('open');
                subLinks.classList.toggle('open');
            });
        }

        // Desktop dropdown - prevent dropdown on mobile view
        const desktopDropdown = document.getElementById('servicesDropdown');
        if (desktopDropdown) {
            desktopDropdown.addEventListener('click', function(e) {
                if (window.innerWidth <= 820) {
                    e.preventDefault();
                    this.classList.toggle('open');
                }
            });
        }
    }
    initDropdownToggle();

    // ============================================================
    // 4. SCROLL REVEAL ANIMATIONS
    // ============================================================
    function initScrollReveal() {
        const animatedElements = document.querySelectorAll(
            '.reveal, .reveal-left, .reveal-right, .drop-animate, .slide-up, .fade-scale, .stagger-children'
        );

        if (animatedElements.length === 0) return;

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, {
            threshold: 0.10,
            rootMargin: '0px 0px -20px 0px'
        });

        animatedElements.forEach(el => observer.observe(el));

        // Handle stagger-children containers
        document.querySelectorAll('.stagger-children').forEach(container => {
            observer.observe(container);
        });

        // Trigger initial animations for elements already in view
        setTimeout(() => {
            animatedElements.forEach(el => {
                const rect = el.getBoundingClientRect();
                if (rect.top < window.innerHeight) {
                    el.classList.add('visible');
                }
            });
        }, 200);
    }
    initScrollReveal();

    // ============================================================
    // 5. COUNTER ANIMATION
    // ============================================================
    function initCounters() {
        const counters = document.querySelectorAll('.counter');
        if (counters.length === 0) return;

        let counterStarted = false;

        const counterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !counterStarted) {
                    counterStarted = true;
                    counters.forEach(counter => {
                        const target = parseInt(counter.getAttribute('data-target'));
                        let current = 0;
                        const increment = Math.ceil(target / 80);

                        const timer = setInterval(() => {
                            current += increment;
                            if (current >= target) {
                                counter.textContent = target;
                                clearInterval(timer);
                            } else {
                                counter.textContent = current;
                            }
                        }, 20);
                    });
                }
            });
        }, { threshold: 0.3 });

        const statsSection = document.querySelector('.stats-showcase, .stats-section');
        if (statsSection) counterObserver.observe(statsSection);
    }
    initCounters();

    // ============================================================
    // 6. OFFICE HOURS STATUS (for contact page)
    // ============================================================
    function updateOfficeStatus() {
        const badge = document.getElementById('statusBadge');
        if (!badge) return;

        const now = new Date();
        const day = now.getDay();
        const hours = now.getHours();
        const minutes = now.getMinutes();
        const timeStr = hours + '.' + (minutes < 10 ? '0' : '') + minutes;

        let isOpen = false;

        // Monday - Friday: 8:00 AM - 5:00 PM
        if (day >= 1 && day <= 5) {
            if (timeStr >= '8.00' && timeStr < '17.00') {
                isOpen = true;
            }
        }
        // Saturday: 9:00 AM - 1:00 PM
        else if (day === 6) {
            if (timeStr >= '9.00' && timeStr < '13.00') {
                isOpen = true;
            }
        }

        if (isOpen) {
            badge.className = 'status-badge open';
            badge.innerHTML = '<i class="fas fa-circle" style="font-size:0.5rem; margin-right:6px;"></i> Open Now';
        } else {
            badge.className = 'status-badge closed';
            badge.innerHTML = '<i class="fas fa-circle" style="font-size:0.5rem; margin-right:6px;"></i> Closed Now';
        }
    }
    updateOfficeStatus();

    // ============================================================
    // 7. TOAST / POPUP SYSTEM
    // ============================================================
    function initToast() {
        const toast = document.getElementById('toast');
        const toastMessage = document.getElementById('toastMessage');
        const toastIcon = document.getElementById('toastIcon');
        const toastClose = document.getElementById('toastClose');

        if (!toast) return;

        let toastTimeout;

        window.showToast = function(message, type = 'success', duration = 5000) {
            clearTimeout(toastTimeout);
            toast.classList.remove('show');

            // Set icon
            const iconMap = {
                success: '<i class="fas fa-check-circle"></i>',
                error: '<i class="fas fa-exclamation-circle"></i>',
                warning: '<i class="fas fa-exclamation-triangle"></i>',
                info: '<i class="fas fa-info-circle"></i>'
            };
            toastIcon.innerHTML = iconMap[type] || iconMap.success;
            toastIcon.className = 'toast-icon ' + type;

            toastMessage.textContent = message;

            // Show toast
            setTimeout(() => {
                toast.classList.add('show');
            }, 100);

            // Auto hide
            toastTimeout = setTimeout(() => {
                toast.classList.remove('show');
            }, duration);
        };

        // Close toast
        if (toastClose) {
            toastClose.addEventListener('click', function() {
                toast.classList.remove('show');
                clearTimeout(toastTimeout);
            });
        }

        // Click outside to close
        toast.addEventListener('click', function(e) {
            if (e.target === this) {
                toast.classList.remove('show');
                clearTimeout(toastTimeout);
            }
        });
    }
    initToast();

    // ============================================================
    // 8. DATE/TIME VALIDATION (for booking page)
    // ============================================================
    function initDateTimeValidation() {
        const dateInput = document.getElementById('preferredDate');
        const timeInput = document.getElementById('preferredTime');
        const dateValidation = document.getElementById('dateValidation');
        const timeValidation = document.getElementById('timeValidation');

        if (!dateInput) return;

        // Set min date to today
        const today = new Date().toISOString().split('T')[0];
        dateInput.setAttribute('min', today);

        function validateDateTime() {
            let isValid = true;

            // Validate date
            const selectedDate = dateInput.value;
            if (selectedDate) {
                const selected = new Date(selectedDate + 'T00:00:00');
                const now = new Date();
                now.setHours(0, 0, 0, 0);
                if (selected < now) {
                    if (dateValidation) dateValidation.classList.add('show');
                    dateInput.style.borderColor = '#e74c3c';
                    isValid = false;
                } else {
                    if (dateValidation) dateValidation.classList.remove('show');
                    dateInput.style.borderColor = '';
                }
            } else {
                if (dateValidation) dateValidation.classList.remove('show');
                dateInput.style.borderColor = '';
            }

            // Validate time (only if date is valid and today)
            const selectedTime = timeInput ? timeInput.value : null;
            if (selectedTime && dateInput.value) {
                const dateStr = dateInput.value;
                const selected = new Date(dateStr + 'T' + selectedTime + ':00');
                const now = new Date();

                const isToday = dateStr === today;
                if (isToday && selected < now) {
                    if (timeValidation) timeValidation.classList.add('show');
                    if (timeInput) timeInput.style.borderColor = '#e74c3c';
                    isValid = false;
                } else {
                    if (timeValidation) timeValidation.classList.remove('show');
                    if (timeInput) timeInput.style.borderColor = '';
                }
            } else {
                if (timeValidation) timeValidation.classList.remove('show');
                if (timeInput) timeInput.style.borderColor = '';
            }

            return isValid;
        }

        dateInput.addEventListener('change', validateDateTime);
        dateInput.addEventListener('input', validateDateTime);
        if (timeInput) {
            timeInput.addEventListener('change', validateDateTime);
            timeInput.addEventListener('input', validateDateTime);
        }

        // Expose validate function globally
        window.validateDateTime = validateDateTime;
    }
    initDateTimeValidation();

    // ============================================================
    // 9. TOGGLE DELIVERY METHOD (booking page - WhatsApp/Email)
    // ============================================================
    function initDeliveryToggle() {
        const toggleWhatsapp = document.getElementById('toggleWhatsapp');
        const toggleEmail = document.getElementById('toggleEmail');
        const deliveryIndicator = document.getElementById('deliveryIndicator');

        if (!toggleWhatsapp || !toggleEmail) return;

        let deliveryMethod = 'whatsapp';

        function setDeliveryMethod(method) {
            deliveryMethod = method;
            toggleWhatsapp.classList.toggle('active', method === 'whatsapp');
            toggleEmail.classList.toggle('active', method === 'email');

            if (deliveryIndicator) {
                if (method === 'whatsapp') {
                    deliveryIndicator.innerHTML =
                        `<i class="fas fa-info-circle"></i> Your request will be sent via <strong class="wa"><i class="fab fa-whatsapp"></i> WhatsApp</strong> to <strong>0790 409 121</strong>`;
                } else {
                    deliveryIndicator.innerHTML =
                        `<i class="fas fa-info-circle"></i> Your request will be sent via <strong class="email"><i class="fas fa-envelope"></i> Email</strong> to <strong>absolomjayson46@gmail.com</strong>`;
                }
            }
        }

        toggleWhatsapp.addEventListener('click', function() {
            setDeliveryMethod('whatsapp');
        });
        toggleEmail.addEventListener('click', function() {
            setDeliveryMethod('email');
        });

        // Expose for other functions
        window.deliveryMethod = deliveryMethod;
        window.setDeliveryMethod = setDeliveryMethod;
    }
    initDeliveryToggle();

    // ============================================================
    // 10. CHARACTER COUNTER (booking/contact form)
    // ============================================================
    function initCharCounter() {
        const messageBox = document.getElementById('messageBox');
        const charCounter = document.getElementById('charCounter');

        if (!messageBox || !charCounter) return;

        function updateCounter() {
            const len = messageBox.value.length;
            charCounter.textContent = len + ' characters';
            charCounter.className = 'char-counter';
            if (len > 80 && len <= 100) {
                charCounter.classList.add('warning');
            } else if (len > 100) {
                charCounter.classList.add('danger');
            }
        }

        messageBox.addEventListener('input', updateCounter);

        // Initial count
        updateCounter();
    }
    initCharCounter();

    // ============================================================
    // 11. CONTACT FORM SUBMISSION (WhatsApp/Email)
    // ============================================================
    function initContactForm() {
        const form = document.getElementById('contactForm');
        const submitBtn = document.getElementById('submitBtn');

        if (!form) return;

        form.addEventListener('submit', function(e) {
            e.preventDefault();

            // Get values
            const name = document.getElementById('fullName')?.value.trim();
            const email = document.getElementById('emailAddress')?.value.trim();
            const phone = document.getElementById('phoneNumber')?.value.trim();
            const subject = document.getElementById('subject')?.value.trim();
            const message = document.getElementById('messageBox')?.value.trim();

            // Validation
            if (!name || !email || !subject || !message) {
                if (typeof showToast === 'function') {
                    showToast('🙏 Please fill in all required fields marked with *', 'warning', 4000);
                }
                return;
            }

            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email)) {
                if (typeof showToast === 'function') {
                    showToast('📧 Please enter a valid email address', 'error', 4000);
                }
                return;
            }

            // Build WhatsApp message
            const waNumber = '254790409121';
            const formattedMessage =
                `📋 *New Contact Message*\n\n` +
                `👤 *Name:* ${name}\n` +
                `✉️ *Email:* ${email}\n` +
                `📱 *Phone:* ${phone || 'Not provided'}\n` +
                `📂 *Subject:* ${subject}\n\n` +
                `💬 *Message:*\n${message}\n\n` +
                `---\nSent from Medrisk Consulting Contact Page`;

            const waMessage = encodeURIComponent(formattedMessage);
            const waUrl = `https://wa.me/${waNumber}?text=${waMessage}`;

            // Open WhatsApp
            window.open(waUrl, '_blank');

            if (typeof showToast === 'function') {
                showToast('✅ WhatsApp opened! Please send the pre-filled message.', 'success', 5000);
            }

            // Feedback on button
            submitBtn.innerHTML = '<i class="fas fa-check"></i> Sent!';
            submitBtn.style.background = '#27ae60';
            setTimeout(() => {
                submitBtn.innerHTML = '<i class="fab fa-whatsapp"></i> Send via WhatsApp';
                submitBtn.style.background = '';
            }, 4000);
        });
    }
    initContactForm();

    // ============================================================
    // 12. BOOKING FORM SUBMISSION
    // ============================================================
    function initBookingForm() {
        const form = document.getElementById('bookingForm');
        const submitBtn = document.getElementById('submitBtn');

        if (!form) return;

        form.addEventListener('submit', function(e) {
            e.preventDefault();

            // Get values
            const fullName = document.getElementById('fullName')?.value.trim();
            const phone = document.getElementById('phoneNumber')?.value.trim();
            const email = document.getElementById('emailAddress')?.value.trim();
            const date = document.getElementById('preferredDate')?.value;
            const time = document.getElementById('preferredTime')?.value;
            const service = document.getElementById('serviceInterest')?.value;
            const message = document.getElementById('messageBox')?.value.trim();

            // Validation
            if (!fullName || !phone || !email || !message) {
                if (typeof showToast === 'function') {
                    showToast('🙏 Please fill in all required fields marked with *', 'warning', 4000);
                }
                return;
            }

            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email)) {
                if (typeof showToast === 'function') {
                    showToast('📧 Please enter a valid email address', 'error', 4000);
                }
                return;
            }

            if (phone.length < 8) {
                if (typeof showToast === 'function') {
                    showToast('📱 Please enter a valid phone number', 'error', 4000);
                }
                return;
            }

            // Validate date/time
            if (typeof window.validateDateTime === 'function') {
                if (!window.validateDateTime()) {
                    if (typeof showToast === 'function') {
                        showToast('⏰ Please select a future date and time', 'warning', 4000);
                    }
                    return;
                }
            }

            // Character detection for WhatsApp
            const charCount = message.length;
            const deliveryMethod = window.deliveryMethod || 'whatsapp';

            if (charCount > 100 && deliveryMethod === 'whatsapp') {
                if (typeof showToast === 'function') {
                    showToast('📝 Your message is over 100 characters. We\'ll switch to Email delivery for you.', 'info', 5000);
                }
                if (typeof window.setDeliveryMethod === 'function') {
                    window.setDeliveryMethod('email');
                }
                setTimeout(() => {
                    submitBooking(fullName, phone, email, date, time, service, message);
                }, 600);
                return;
            }

            submitBooking(fullName, phone, email, date, time, service, message);
        });
    }

    function submitBooking(fullName, phone, email, date, time, service, message) {
        const submitBtn = document.getElementById('submitBtn');
        const serviceText = service || 'Not specified';
        const dateText = date || 'Not specified';
        const timeText = time || 'Not specified';

        const formattedMessage =
            `📋 *New Booking Request*\n\n` +
            `👤 *Name:* ${fullName}\n` +
            `📱 *Phone:* ${phone}\n` +
            `✉️ *Email:* ${email}\n` +
            `📅 *Date:* ${dateText}\n` +
            `🕐 *Time:* ${timeText}\n` +
            `📂 *Service:* ${serviceText}\n\n` +
            `💬 *Message:*\n${message}\n\n` +
            `---\nSent from Medrisk Consulting Booking Page`;

        const deliveryMethod = window.deliveryMethod || 'whatsapp';

        if (deliveryMethod === 'whatsapp') {
            const waNumber = '254790409121';
            const waMessage = encodeURIComponent(formattedMessage);
            const waUrl = `https://wa.me/${waNumber}?text=${waMessage}`;
            window.open(waUrl, '_blank');

            if (typeof showToast === 'function') {
                showToast('✅ WhatsApp opened! Please send the pre-filled message.', 'success', 5000);
            }
        } else {
            const recipientEmail = 'absolomjayson46@gmail.com';
            const subject = encodeURIComponent(`Booking Request from ${fullName}`);
            const emailBody = encodeURIComponent(
                `New Booking Request\n\n` +
                `Name: ${fullName}\n` +
                `Phone: ${phone}\n` +
                `Email: ${email}\n` +
                `Preferred Date: ${dateText}\n` +
                `Preferred Time: ${timeText}\n` +
                `Service Interest: ${serviceText}\n\n` +
                `Message:\n${message}\n\n` +
                `---\nSent from Medrisk Consulting Booking Page`
            );
            const mailtoLink = `mailto:${recipientEmail}?subject=${subject}&body=${emailBody}`;
            window.location.href = mailtoLink;

            if (typeof showToast === 'function') {
                showToast('📧 Email client opened! Please send the message.', 'success', 5000);
            }
        }

        // Feedback on button
        if (submitBtn) {
            submitBtn.innerHTML = '<i class="fas fa-check"></i> Sent!';
            submitBtn.style.background = '#27ae60';
            setTimeout(() => {
                submitBtn.innerHTML = '<i class="fas fa-paper-plane"></i> Send Request';
                submitBtn.style.background = '';
            }, 4000);
        }
    }
    initBookingForm();

    // ============================================================
    // 13. VIDEO FALLBACK (hero background)
    // ============================================================
    function initVideoFallback() {
        const video = document.querySelector('.hero-video-wrapper video');
        if (video) {
            video.addEventListener('error', function() {
                this.style.display = 'none';
                const hero = document.querySelector('.hero');
                if (hero) {
                    hero.style.background = 'url(images/hero-home.jpg) center center / cover no-repeat';
                }
            });
        }
    }
    initVideoFallback();

    // ============================================================
    // 14. SMOOTH SCROLL FOR ANCHOR LINKS
    // ============================================================
    function initSmoothScroll() {
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const href = this.getAttribute('href');
                if (href === "#" || href === "") return;

                // Skip if it's a dropdown toggle or has preventDefault already
                if (this.classList.contains('dropdown-label')) return;

                e.preventDefault();
                const target = document.querySelector(href);
                if (target) {
                    const offset = 100;
                    const top = target.getBoundingClientRect().top + window.pageYOffset - offset;
                    window.scrollTo({ top, behavior: 'smooth' });
                }
            });
        });
    }
    initSmoothScroll();

    // ============================================================
    // 15. NAVBAR SCROLL EFFECT (optional - adds shadow on scroll)
    // ============================================================
    function initNavbarScroll() {
        const navbar = document.querySelector('.navbar');
        if (!navbar) return;

        window.addEventListener('scroll', function() {
            if (window.scrollY > 50) {
                navbar.style.boxShadow = '0 10px 40px rgba(0,0,0,0.08)';
            } else {
                navbar.style.boxShadow = '0 10px 30px rgba(17, 82, 118, 0.08)';
            }
        });
    }
    initNavbarScroll();

    // ============================================================
    // 16. PARALLAX / SCROLL EFFECTS (optional enhancement)
    // ============================================================
    function initParallaxEffects() {
        // Add subtle parallax to floating shapes
        const shapes = document.querySelectorAll('.shape, .hero-float');
        if (shapes.length === 0) return;

        window.addEventListener('scroll', function() {
            const scrolled = window.pageYOffset;
            shapes.forEach((shape, index) => {
                const speed = 0.02 + (index * 0.01);
                const yPos = scrolled * speed;
                shape.style.transform = `translateY(${yPos}px)`;
            });
        });
    }
    initParallaxEffects();

    // ============================================================
    // 17. KEYBOARD ACCESSIBILITY (Escape key closes mobile menu)
    // ============================================================
    function initKeyboardAccessibility() {
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                const overlay = document.getElementById('mobileOverlay');
                if (overlay && overlay.classList.contains('open')) {
                    overlay.classList.remove('open');
                    const hamburger = document.getElementById('hamburger');
                    if (hamburger) hamburger.classList.remove('active');
                }
            }
        });
    }
    initKeyboardAccessibility();

    // ============================================================
    // 18. WINDOW RESIZE HANDLER (close mobile menu on resize)
    // ============================================================
    function initResizeHandler() {
        let resizeTimeout;
        window.addEventListener('resize', function() {
            clearTimeout(resizeTimeout);
            resizeTimeout = setTimeout(() => {
                if (window.innerWidth > 820) {
                    const overlay = document.getElementById('mobileOverlay');
                    if (overlay && overlay.classList.contains('open')) {
                        overlay.classList.remove('open');
                        const hamburger = document.getElementById('hamburger');
                        if (hamburger) hamburger.classList.remove('active');
                    }
                }
            }, 300);
        });
    }
    initResizeHandler();

    // ============================================================
    // 19. LAZY LOAD IMAGES (performance optimization)
    // ============================================================
    function initLazyLoad() {
        const images = document.querySelectorAll('img[data-src]');
        if (images.length === 0) return;

        const imageObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const img = entry.target;
                    img.src = img.getAttribute('data-src');
                    img.removeAttribute('data-src');
                    imageObserver.unobserve(img);
                }
            });
        }, { threshold: 0.1 });

        images.forEach(img => imageObserver.observe(img));
    }
    initLazyLoad();

    // ============================================================
    // 20. SERVICE CARD HOVER EFFECT (for service-detail page)
    // ============================================================
    function initServiceCardEffects() {
        const cards = document.querySelectorAll('.service-card-modern, .service-block');
        cards.forEach(card => {
            card.addEventListener('mouseenter', function() {
                // Optional: add additional effects
            });
            card.addEventListener('mouseleave', function() {
                // Optional: remove effects
            });
        });
    }
    initServiceCardEffects();

    // ============================================================
    // 21. PAYMENT PAGE SPECIFIC (redirect if needed)
    // ============================================================
    function initPayPage() {
        // Check if on pay.html
        if (window.location.pathname.includes('pay.html')) {
            // Any specific pay page functionality
            console.log('Payment page loaded');
        }
    }
    initPayPage();

    // ============================================================
    // 22. CONSOLE LOG (development info - remove in production)
    // ============================================================
    console.log('✅ Medrisk Consulting - Scripts loaded successfully');
    console.log('📅 ' + new Date().toLocaleString());

}); // End of DOMContentLoaded