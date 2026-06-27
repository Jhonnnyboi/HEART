<h1>HAHA, HEARTDAWG</h1>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ILOVEYA Heart</title>

<style>
    body{
        margin:0;
        background:#000;
        color:#ff4d6d;
        display:flex;
        justify-content:center;
        align-items:center;
        height:100vh;
        overflow:hidden;
        font-family:monospace;
        white-space:pre;
        font-size:12px;
        line-height:12px;
    }

    #heart{
        text-align:center;
    }
</style>
</head>
<body>

<pre id="heart"></pre>

<script>
const text = "ILOVEYA ";
const heart = document.getElementById("heart");

let output = "";

for(let y = 1.5; y > -1.5; y -= 0.08){
    for(let x = -1.5; x < 1.5; x += 0.04){

        let a = x*x + y*y - 1;
        let formula = a*a*a - x*x*y*y*y;

        if(formula <= 0){
            output += text[(Math.floor((x-y)*20)) % text.length];
        }else{
            output += " ";
        }
    }
    output += "\n";
}

heart.textContent = output;
</script>

</body>
</html>
