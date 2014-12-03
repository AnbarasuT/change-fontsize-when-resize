change-fontsize-when-resize
===========================

font size change



$(function() {
    $(window).bind('resize', function()
    {
        resizeMe();
        }).trigger('resize');
    });




function resizeMe() {
    //Standard height, for which the body font size is correct
    var preferredHeight = 768;
    //Base font size for the page
    var fontsize = 14;
    var displayHeight = $(window).height();
    var percentage = displayHeight / preferredHeight;
    var newFontSize = Math.floor(fontsize * percentage) - 1;
    alert(newFontSize)
    $("body").css("font-size", newFontSize);
}

