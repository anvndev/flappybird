# flappybird

link: https://anvndev.github.io/flappybird/

````html
   // Hàm va chạm giữa 2 object
    function collision($div1, $div2) {
        // Khai báo các thông số của 2 object
        var x1 = $div1.offset().left;
        var y1 = $div1.offset().top;
        var h1 = $div1.outerHeight(true);
        var w1 = $div1.outerWidth(true);
        var b1 = y1 + h1;
        var r1 = x1 + w1;
        
        var x2 = $div2.offset().left;
        var y2 = $div2.offset().top;
        var h2 = $div2.outerHeight(true);
        var w2 = $div2.outerWidth(true);
        var b2 = y2 + h2;
        var r2 = x2 + w2;

        // Nếu xảy ra va chạm
        if (b1 < y2 || y1 > b2 || r1 < x2 || x1 > r2) {
            return false;
        }
        // Ngược lại không va chạm
        else
        {
            return true;
        }
    }
