# agar.io hacks
agar.io hacks (tampermonky)



install tampermonky on chrome web store
open tampermonky and click create new script  
install this url code in tampermonky (copy/paste)
click file and click save now enjoy
(if this works pls star this prodject)

var intr,intr1,intr2,intr3,intr4,ovrClk;
var bool = [false,false,false,false,false,false,false,false,false,false,false,false,false];
var carr = false;
var off = false;
var disable_S = false;
var clk = [1,50];
var step = 1;
$(document).on('keydown',function(key) {
    this.key = key.keyCode;
    if(key.keyCode == 49) {
        bool[0] = true;
        if(bool[1]) {
            return;
        }
        bool[1] = true;
        if(bool[0]) {
            ovrClk = setInterval(function() {
                off = true;
                bool[4] = true;
                bool[5] = false;
                bool[6] = false;
                bool[7] = false;
                bool[8] = false;
                bool[9] = false;
                clk[0] = 10000;
                clearInterval(intr);
                clearInterval(intr1);
                return;
            }, 0.05);
        }
    }else if(key.keyCode == 51) {
        bool[2] = true;
        if(bool[3]) {
            return;
        }
        bool[3] = true;
        if(bool[2]) {
            ovrclk1 = setInterval(function() {
                disable_S = true;
                clk[1] = 1000000;
            }, 0.05);
        }
    }else if(key.keyCode == 48) {
        if(step == 1) {
            off = false;
