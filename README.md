<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Beating Heart — Demo</title>
    <style>
        :root{
            --heart-color: #490505;
            --beat-duration: 0.8s;
        }

        html,body{
            height:100%;margin:0;
            font-family:system-ui,-apple-system,Segoe UI,Roboto,'Palace Script MT',Harrington;
        }
        .page{
            min-height:100%;
            display:flex;align-items:center;justify-content:center;flex-direction:column;
            background:linear-gradient(180deg, #ffa5a5 0%, #556e73 100%);
            color: #000000;
            padding:36px;box-sizing:border-box;
        }

        .card{
            background:linear-gradient(180deg, rgb(44, 3, 3), rgb(64, 12, 12));
            border-radius:18px;padding:28px;
            box-shadow:0 10px 30px rgb(94, 8, 8);
            display:flex;gap:24px;align-items:center;flex-direction:column;
            width:clamp(320px, 60vw, 640px);
        }

        .heart-wrap{
            display:flex;flex-direction:column;align-items:center;gap:20px;
        }

        .heart{
            width:180px;height:200px;
            display:block;
            transform-origin:center center;
            animation:beat var(--beat-duration) infinite cubic-bezier(.215,.61,.355,1);
            filter:drop-shadow(0 6px 18px rgb(237, 14, 14));
        }

        .heart path{
            fill:var(--heart-color);
            transition:fill .25s ease;
        }

        @keyframes beat{
            0%{transform:scale(1)}
            8%{transform:scale(1.25)}
            18%{transform:scale(0.9)}
            42%{transform:scale(1)}
            100%{transform:scale(1)}
        }

        .love-text {
            font-size: 1.8rem;
            font-weight: bold;
            text-align: center;
            color: #edc846;
            text-shadow: 0 0 10px rgba(251, 239, 100, 0.6);
            animation: fadeGlow 2s ease-in-out infinite alternate;
            font-family: "Kirgina";
        }


        @media (max-width:420px){
            .heart{width:180px;height:180px}
            .love-text { font-size: 1.2rem; }
        }
    </style>
</head>
<body>
<main class="page">
    <div class="card" role="region" aria-label="Beating heart demo">
        <div class="heart-wrap">
            <!-- Larger, more curved SVG heart -->
            <svg class="heart" viewBox="0 0 512 512" role="img" aria-labelledby="heartTitle heartDesc">
                <title id="heartTitle">Beating heart</title>
                <desc id="heartDesc">A pulsing, full heart shape that simulates a heartbeat.</desc>
                <path d="M471.7 73.1c-54.5-46.4-136-38.3-186.4 13.7L256 116.3l-29.3-29.5C176.3 34.8 94.8 26.7 40.3 73.1c-62.1 52.9-66.5 149.8-9.9 207.3l193.5 198.3c17.4 17.8 45.6 17.8 63 0l193.5-198.3c56.6-57.5 52.2-154.4-9.7-207.3z"/>
            </svg>

            <div class="love-text">Te amo mi corazón de melón, Edsson &lt;55 </div>
        </div>
    </div>
</main>
<div class="love-text">te doy mi corazon, mi hombre guapo, hermoso, trabajor e imparable, MWAH! </div>
</div>
</div>
</main>

<script>
    const heart = document.querySelector('.heart');
    heart.style.animationPlayState = 'running';
</script>
</body>
</html>
