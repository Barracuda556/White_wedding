// Модальное окно
$('.open-modal').click(function() {
    $('.sm-questionnaire').addClass('sm-open')
    $('body').addClass('lock')
    $('html.animating [data-jsscroll]:not([data-jsscroll_nomob])').css('opacity','1')
})

$('.sm-quest-modal-close').click(function() {
    $('.sm-quest-modal').removeClass('sm-open')
    $('body').removeClass('lock')
})

const wishSliderParams = {
    slidesToShow: 1,
    infinite: true,
    adaptiveHeight: false,
    nextArrow: $('#wishes-navigation .sm-arrow-next'),
    prevArrow: $('#wishes-navigation .sm-arrow-prev'),
}

function onResize(){

    $('.sm-dress-code__slider1').slick({
        slidesToShow: 1,
        infinite: true,
        adaptiveHeight: true,
        nextArrow: $('.sm-dress-code__slider1').parents('.sm-dress-code__box-gallery__item').find('.sm-arrow-next'),
        prevArrow: $('.sm-dress-code__slider1').parents('.sm-dress-code__box-gallery__item').find('.sm-arrow-prev'),
    });

    $('.sm-dress-code__slider2').slick({
        slidesToShow: 1,
        infinite: true,
        adaptiveHeight: true,
        nextArrow: $('.sm-dress-code__slider2').parents('.sm-dress-code__box-gallery__item').find('.sm-arrow-next'),
        prevArrow: $('.sm-dress-code__slider2').parents('.sm-dress-code__box-gallery__item').find('.sm-arrow-prev'),
    });

}
//
// $(window).on('resize', function() {
//     onResize();
// });
function startAll() {
    startAllScripts();
    onResize();
}
const forms = document.querySelectorAll('.contact-form');
const thankYouMessage = document.getElementById('thankYouMessage');
const body = document.body;

// Обрабатываем каждую форму
forms.forEach(form => {

    form.addEventListener('submit', function(event) {
        event.preventDefault(); // предотвращаем отправку формы по умолчанию
        thankYouMessage.classList.add('sm-open'); // показываем сообщение
        body.classList.add('sm-hidde'); // добавляем класс sm-hidde к body
        form.reset(); // очищаем форму
    });
});
// Закрываем модальное сообщение
$(".sm-modal-close").on('click', function() {
    console.log('close__modal');
    $(this).closest('.sm-modal.sm-open').removeClass('sm-open');
    $('body').removeClass('lock');
    $('.f-button.is-close-btn').css('display','none');
})

$(window).on('load', function() {
    setTimeout(function(){
        console.log('len: '+$('.sm-dress-code__colors .sm_colors div').length);
        $('.sm_colors div').each(function (color) {
            if($(this).css('background')==$('.sm-dress-code').css('background')){
                console.log($(this).css('background')+' | '+$('.sm-dress-code').css('background'));
                $(this).css('border','solid 1px #262222');
            }
        });
    },700);
});
