// items animate
// function isElementInViewport(el, offset = 0) {
//     let rect = el.getBoundingClientRect();
//     return (
//         rect.top <= (window.innerHeight + offset) &&
//         rect.bottom >= (0 - offset)
//     );
// }
// window.addEventListener('load', function() {
// 	this.alert(window.innerHeight)
//     let items = document.querySelectorAll('.item-animation');
//     if (items) {
//         items.forEach(function(item) {
//             if (isElementInViewport(item)) {
//                 item.classList.add('item-active');
//             }
//         });
//     }
// });
let lastScrollY = window.scrollY;
let currentSlide = 0
function checkVisibilityEr(element, callback, offset = 0) {

    const rect = element.getBoundingClientRect();
    const isVisible = (     rect.top <= (window.innerHeight + offset) &&         rect.bottom >= (0 - offset))
    if (isVisible) callback();
}

var isThrottleder = false;
$(function(){
    setTimeout(function(){
        var checkIntro = setInterval(function(){
            if(!$(body).hasClass('opener-active')) {
                handleScroller()
                clearInterval(checkIntro);
            }
        }, 500)
    },1000);
})
window.addEventListener('scroll',  () => {if (!isThrottleder) {
    handleScroller();
    isThrottleder = true;
    setTimeout(() => { isThrottleder = false; }, 100);
}})

window.addEventListener('scroll',  () => {
    const currentScrollY = window.scrollY;
    const scrollDelta = currentScrollY - lastScrollY;

    // const rotationSpeed = 0.2;
    currentSlide += scrollDelta*0.6;
    document.querySelectorAll('.sm-email-back.back-2').forEach(item => {
        console.log(document.documentElement.clientHeight+ ' | '+item.getBoundingClientRect().top);
        if((document.documentElement.clientHeight/2 - (document.documentElement.clientHeight/4)) < item.getBoundingClientRect().top && (document.documentElement.clientHeight/2) > item.getBoundingClientRect().top) {
            item.style.top = (item.getBoundingClientRect().top-(document.documentElement.clientHeight/2 - (document.documentElement.clientHeight/4)))*(80/(document.documentElement.clientHeight/4))+'px';
            console.log('animate')
            // item.style.transition = 'transform 0.1s ease-out';
        }
        else
        {
            $('.item-animation_new:not(.item-active)').toggleClass('item-active',true)
        }
    });
    lastScrollY = currentScrollY;
})
// window.addEventListener('load',  () => {if (!isThrottleder) {
//     handleScroller();
//
//     isThrottleder = true;
//     setTimeout(() => { isThrottleder = false; }, 100);
// }})
window.addEventListener('resize', () => { if (!isThrottleder) {
    handleScroller();

    isThrottleder = true;
    setTimeout(() => { isThrottleder = false; }, 100);
}})

function handleScroller() {
    if(!$(body).hasClass('opener-active')) {
        document.querySelectorAll('.item-animation').forEach(el => {
            checkVisibilityEr(el, () => {
                el.classList.add('item-active');
            });
        });
    }
}

$('.sm-form_checkbox_box').on('click', function() {
    const $radio = $(this).prev('.sm-form_checkbox_input');
    if ($radio.attr('type') === 'radio') {
        $radio.prop('checked', true);
    } else if ($radio.attr('type') === 'checkbox') {
        $radio.prop('checked', !$radio.prop('checked'));
    }
});



// window.addEventListener('scroll', function() {
//     let items = document.querySelectorAll('.item-animation');
//     if (items) {
//         items.forEach(function(item) {
//             if (isElementInViewport(item)) {
//                 item.classList.add('item-active');
//             }
//         });
//     }
// });