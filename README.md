<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Sumi's Birthday | Bestie Vibes & Compliments 🎀</title>
    <!-- Vintage Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Kalam:wght@300;400;700&family=Caveat:wght@400;700&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            background: #fdf3e3;
            background-image: radial-gradient(circle at 20% 35%, rgba(210, 170, 100, 0.12) 2%, transparent 2.5%),
                              repeating-linear-gradient(45deg, rgba(190, 145, 85, 0.05) 0px, rgba(190, 145, 85, 0.05) 2px, transparent 2px, transparent 10px);
            font-family: 'Special Elite', 'Courier New', monospace;
            color: #3b2a1f;
            padding: 1.2rem;
            position: relative;
        }

        .main-wrapper {
            max-width: 1400px;
            margin: 0 auto;
            background: rgba(254, 248, 235, 0.92);
            border-radius: 32px 32px 60px 60px;
            box-shadow: 0 25px 45px rgba(0, 0, 0, 0.1);
            padding: 1.8rem;
            backdrop-filter: blur(2px);
            border: 1px solid #ecdbba;
        }

        .hero {
            text-align: center;
            border-bottom: 2px dashed #e2caa0;
            padding-bottom: 1.2rem;
            margin-bottom: 1.8rem;
        }

        .cursive-big {
            font-family: 'Caveat', cursive;
            font-size: 4rem;
            font-weight: 700;
            background: linear-gradient(135deg, #bc6f3a, #e7a062);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .typewriter-date {
            font-family: 'Special Elite', monospace;
            background: #f2e3cf;
            display: inline-block;
            padding: 0.3rem 1.5rem;
            border-radius: 50px;
            margin-top: 10px;
            font-size: 0.9rem;
        }

        .doodle-row {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin: 15px 0 8px;
            font-size: 1.8rem;
        }

        /* friendship banner */
        .friendship-banner {
            background: #fef5e8;
            border-radius: 30px;
            padding: 0.8rem;
            text-align: center;
            margin-bottom: 1.8rem;
            border-left: 8px solid #9bc48e;
        }

        /* PHOTO GALLERY - each photo has a unique compliment */
        .gallery-title {
            text-align: center;
            font-family: 'Caveat', cursive;
            font-size: 2rem;
            margin: 1.5rem 0 1rem;
        }

        .polaroid-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
            gap: 28px;
            justify-items: center;
            margin: 1.5rem 0;
        }

        .polaroid {
            background: #fffcf3;
            padding: 14px 14px 20px 14px;
            box-shadow: 8px 12px 20px rgba(0, 0, 0, 0.12);
            transform: rotate(var(--rot, 0deg));
            transition: all 0.3s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            width: 100%;
            max-width: 230px;
            border-radius: 18px 18px 24px 24px;
            border: 1px solid #f2e2c0;
            cursor: pointer;
        }

        .polaroid:hover {
            transform: rotate(0deg) scale(1.02);
            box-shadow: 12px 18px 28px rgba(0, 0, 0, 0.15);
        }

        .polaroid img {
            width: 100%;
            aspect-ratio: 1 / 1;
            object-fit: cover;
            border-radius: 14px;
            filter: sepia(0.15) contrast(1.03) brightness(1.01);
            background: #cfb78b;
        }

        .polaroid-caption {
            text-align: center;
            margin-top: 12px;
            font-family: 'Kalam', cursive;
            font-size: 1rem;
            font-weight: bold;
            color: #aa6a3c;
            transition: 0.2s;
        }

        .compliment-badge {
            display: inline-block;
            background: #f5e6d4;
            border-radius: 40px;
            padding: 4px 12px;
            font-size: 0.75rem;
            margin-top: 6px;
            font-family: monospace;
        }

        /* extra cute activities (mini games) */
        .activities-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin: 2rem 0 1rem;
            justify-content: center;
        }

        .mini-card {
            background: #fffbf0;
            border-radius: 28px;
            padding: 0.8rem 1.2rem;
            flex: 1;
            min-width: 150px;
            text-align: center;
            border: 1px solid #f3e2c5;
            transition: 0.2s;
        }
        .mini-card:hover { transform: translateY(-3px);}

        .fortune-btn, .compliment-btn {
            background: #c9865c;
            border: none;
            color: white;
            padding: 6px 16px;
            border-radius: 30px;
            cursor: pointer;
            font-family: monospace;
            margin-top: 8px;
        }

        .floating-emoji {
            position: fixed;
            pointer-events: none;
            z-index: 10000;
            font-size: 1.5rem;
            animation: floatUp 2.5s ease-out forwards;
        }

        @keyframes floatUp {
            0% { transform: translateY(0) scale(0.4); opacity: 0.9; }
            100% { transform: translateY(-400px) scale(1.1); opacity: 0; }
        }

        footer {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.7rem;
            border-top: 1px dashed #dec394;
            padding-top: 1rem;
        }

        @media (max-width: 650px) {
            .polaroid-grid { gap: 16px; }
            .cursive-big { font-size: 2.8rem; }
        }
    </style>
</head>
<body>

<div class="main-wrapper">
    <div class="hero">
        <div class="doodle-row">🎈🍒📸🧸🌸🍰🎀🐻‍❄️🍬✨</div>
        <div class="cursive-big">🎉 Happy Birthday, Sumi! 🎉</div>
        <div class="typewriter-date"><i class="fas fa-calendar-alt"></i> 14th June — Bestie Birthday Bash! <i class="fas fa-star"></i></div>
        <div class="doodle-row">📸✨🎀</div>
    </div>

    <!-- Friendship note (platonic) -->
    <div class="friendship-banner">
        <i class="fas fa-handshake"></i> To my amazing friend Sumi — you're the best! Hope your day is filled with laughs, cake, and good vibes. <i class="fas fa-heart" style="color:#9bc48e;"></i> — Subho
    </div>

    <!-- PHOTO GALLERY with 10 PHOTOS + UNIQUE COMPLIMENT UNDER EACH -->
    <div class="gallery-title">
        <i class="fas fa-camera-retro"></i> 10 precious moments with Sumi <i class="fas fa-heart" style="color:#e8a87c;"></i>
    </div>
    <div class="polaroid-grid" id="polaroidGrid"></div>
    <p style="text-align: center; font-size: 0.7rem; margin-top: -0.5rem; margin-bottom: 1rem;">
        <i class="fas fa-star"></i> each photo has a special compliment — click any photo to see the magic! <i class="fas fa-star"></i>
    </p>

    <!-- Extra cute mini activities (no romance, just fun) -->
    <div class="activities-row">
        <div class="mini-card">
            <i class="fas fa-cookie-bite fa-2x"></i>
            <div id="fortuneMsg" style="font-size:0.8rem; margin:8px 0;">🌸 sweet message</div>
            <button class="fortune-btn" id="fortuneBtn"><i class="fas fa-hand-peace"></i> Fortune Cookie</button>
        </div>
        <div class="mini-card">
            <i class="fas fa-gift fa-2x"></i>
            <div id="giftMsg" style="font-size:0.8rem; margin:8px 0;">🎁 open a gift</div>
            <button class="compliment-btn" id="giftBtn"><i class="fas fa-gift"></i> Open Gift</button>
        </div>
        <div class="mini-card">
            <i class="fas fa-cat fa-2x"></i>
            <div id="catMsg" style="font-size:0.8rem; margin:8px 0;">🐱 pet the kitty</div>
            <button class="compliment-btn" id="petCatBtn"><i class="fas fa-paw"></i> Pet Cat</button>
        </div>
        <div class="mini-card">
            <i class="fas fa-smile fa-2x"></i>
            <div id="complimentMsg" style="font-size:0.8rem; margin:8px 0;">💬 nice words</div>
            <button class="compliment-btn" id="randomComplimentBtn"><i class="fas fa-star"></i> Compliment</button>
        </div>
    </div>

    <footer>
        <i class="fas fa-feather-alt"></i> made with doodles & bestie energy — for Sumi's 14th June 🎉
        <br>✨ click any polaroid to see a unique compliment! ✨
    </footer>
</div>

<script>
    // ============================================================
    // 10 PHOTOS WITH UNIQUE, PLATONIC COMPLIMENTS (one per photo)
    // Each photo has a different compliment - displayed when clicked
    // ============================================================
    
    // Array of 10 unique compliments (friendly, sweet, no romance)
    const uniqueCompliments = [
        "🌸 You have the kindest heart! Always makes everyone feel welcome.",
        "🍰 You're literally the funniest person I know — your memes are iconic!",
        "🎀 Your energy is so positive and uplifting. Thanks for being you!",
        "🧸 You're an amazing friend — so loyal, honest, and real. No cap!",
        "✨ Your smile lights up any room. Keep shining bestie!",
        "🍒 You're so creative and talented! Everything you do is awesome.",
        "📸 You have the best vibes — hanging out with you is always a blast!",
        "🐻‍❄️ You're so strong and brave. I admire you a lot!",
        "💛 You make the world a better place just by being in it. Periodt.",
        "🎉 You're the coolest person to have late night chats with. Bestie forever!"
    ];
    
    // Captions for each photo (short & sweet)
    const photoCaptions = [
        "🌸 sunny days", "🍰 cake time", "🎀 cute moment", "🧸 cozy vibes", 
        "✨ sparkle energy", "🍒 fun times", "📸 memory lane", "🐻‍❄️ adventure", 
        "💛 happy heart", "🎉 celebration"
    ];
    
    // Placeholder image URLs (vintage style SVGs - easily replaceable with actual photos)
    // Using beautiful pastel placeholder SVGs with photo frame look
    const placeholderColors = ["#faeedb", "#fef0e2", "#fcf1e6", "#faf0e3", "#fdf2e8", "#fff4ea", "#fef3e6", "#faf1e4", "#fdf0e0", "#fff2e6"];
    
    const polaroidGrid = document.getElementById('polaroidGrid');
    
    for (let i = 0; i < 10; i++) {
        const polaroid = document.createElement('div');
        polaroid.className = 'polaroid';
        // random rotation for vintage feel
        const rot = (Math.random() * 6 - 3).toFixed(1);
        polaroid.style.setProperty('--rot', `${rot}deg`);
        
        // Create image with vintage SVG placeholder
        const img = document.createElement('img');
        const bgColor = placeholderColors[i % placeholderColors.length];
        // Cute SVG placeholder with photo frame and "Sumi" label
        const svgContent = `
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 220 220" width="220" height="220">
            <rect width="220" height="220" fill="${bgColor}" rx="16" ry="16"/>
            <rect x="12" y="12" width="196" height="160" rx="14" fill="#fff7ef" stroke="#d9b68c" stroke-width="1.5" stroke-dasharray="6 4"/>
            <circle cx="110" cy="90" r="32" fill="#ffe8d4" stroke="#cb9b6b" stroke-width="1.5"/>
            <text x="110" y="72" font-family="'Special Elite', monospace" font-size="13" fill="#a76f46" text-anchor="middle">📸 Sumi ${i+1}</text>
            <text x="110" y="120" font-family="'Caveat', cursive" font-size="24" fill="#bf7a4a" text-anchor="middle">🌸✨</text>
            <path d="M45 195 L175 195" stroke="#e2c6a0" stroke-width="1.5" stroke-dasharray="4 3"/>
        </svg>`;
        img.src = 'data:image/svg+xml,' + encodeURIComponent(svgContent);
        img.alt = `Sumi's memory ${i+1}`;
        
        // Caption div (shows short label + will show compliment on click)
        const captionDiv = document.createElement('div');
        captionDiv.className = 'polaroid-caption';
        captionDiv.innerHTML = `<i class="fas fa-heart" style="color:#e6905f;"></i> ${photoCaptions[i]} <i class="fas fa-heart" style="color:#e6905f;"></i>
                                <div class="compliment-badge" id="complimentBadge${i}">✨ tap for compliment ✨</div>`;
        
        polaroid.appendChild(img);
        polaroid.appendChild(captionDiv);
        
        // Add click event to show the unique compliment for THIS photo
        const complimentBadge = captionDiv.querySelector(`.compliment-badge`);
        polaroid.addEventListener('click', (function(index) {
            return function() {
                // Show the unique compliment
                complimentBadge.innerHTML = `💬 "${uniqueCompliments[index]}" 💬`;
                complimentBadge.style.background = "#e8d5b8";
                complimentBadge.style.color = "#8b5a3a";
                // Add floating emoji for extra cuteness
                createFloatingEmoji('💛');
                // Reset after 3 seconds to original text? but keep compliment visible for a while, then revert after 4 sec
                setTimeout(() => {
                    if (complimentBadge.innerHTML !== `✨ tap for compliment ✨`) {
                        complimentBadge.innerHTML = `✨ tap for compliment ✨`;
                        complimentBadge.style.background = "#f5e6d4";
                    }
                }, 4000);
            };
        })(i));
        
        polaroidGrid.appendChild(polaroid);
    }
    
    // Also add a note in console for replacing with real photos
    console.log("🎀 To add Sumi's real photos: replace the img src inside each .polaroid with your image URLs! The 10 unique compliments will stay with each photo.");
    
    // ========== EXTRA FUN ACTIVITIES (platonic) ==========
    
    // 1. Fortune Cookie messages
    const fortuneMessages = [
        "🌸 Wishing you the happiest birthday ever, bestie!",
        "🍰 This year will bring you so much joy and success!",
        "🎀 You're the coolest friend anyone could ask for ✨",
        "🧸 May your day be filled with cake, laughs, and good vibes!",
        "💛 You deserve all the amazing things coming your way!",
        "🍒 No cap, you're literally the best. Keep shining!",
        "📸 More fun memories and adventures await you this year!",
        "🐻‍❄️ You're iconic, don't ever change bestie!"
    ];
    const fortuneBtn = document.getElementById('fortuneBtn');
    const fortuneMsgDiv = document.getElementById('fortuneMsg');
    fortuneBtn.addEventListener('click', () => {
        const random = fortuneMessages[Math.floor(Math.random() * fortuneMessages.length)];
        fortuneMsgDiv.innerHTML = `🍪 "${random}" 🍪`;
        createFloatingEmoji('🍀');
    });
    
    // 2. Gift button
    const giftBtn = document.getElementById('giftBtn');
    const giftMsgDiv = document.getElementById('giftMsg');
    const giftItems = ["🎁 Virtual cupcake! 🧁", "📸 A cute photo frame sticker!", "🌸 A virtual bouquet of flowers!", "🍰 Digital birthday cake slice!", "✨ Sparkle jar (full of good vibes)!", "🎀 A shiny virtual hair clip!"];
    let giftIdx = 0;
    giftBtn.addEventListener('click', () => {
        giftMsgDiv.innerHTML = `🎁 ${giftItems[giftIdx % giftItems.length]} 🎁`;
        createFloatingEmoji('🎁');
        giftIdx++;
    });
    
    // 3. Pet the cat button
    let petCount = 0;
    const petCatBtn = document.getElementById('petCatBtn');
    const catMsgDiv = document.getElementById('catMsg');
    petCatBtn.addEventListener('click', () => {
        petCount++;
        catMsgDiv.innerHTML = `🐱 You petted the kitty ${petCount} time${petCount !== 1 ? 's' : ''}! It purrs happily! 🐾`;
        createFloatingEmoji('🐱');
        setTimeout(() => {
            if (petCount % 3 === 0) catMsgDiv.innerHTML = `🐱💖 Kitty loves you bestie! 💖🐱`;
            else catMsgDiv.innerHTML = `🐱 kitty says meow! 😸`;
        }, 1500);
        setTimeout(() => {
            if (petCount % 2 === 0) catMsgDiv.innerHTML = `🐱💤 happy cat`;
            else catMsgDiv.innerHTML = `🐱✨ purr machine`;
        }, 3000);
    });
    
    // 4. Random Compliment button (extra compliments)
    const extraCompliments = [
        "🌸 You're such a kind soul!", "🍰 Your smile makes everyone's day!", "🎀 You're literally the coolest bestie!",
        "✨ You have amazing vibes!", "🧸 You're so fun to be around!", "🍒 You're iconic, no cap!",
        "📸 You take the best selfies!", "💛 Thanks for being an awesome friend!", "🐻‍❄️ You're so strong and inspiring!",
        "🎉 You make every hangout 10x better!"
    ];
    const randomComplimentBtn = document.getElementById('randomComplimentBtn');
    const complimentMsgDiv = document.getElementById('complimentMsg');
    randomComplimentBtn.addEventListener('click', () => {
        const randomComp = extraCompliments[Math.floor(Math.random() * extraCompliments.length)];
        complimentMsgDiv.innerHTML = `💬 "${randomComp}" 💬`;
        createFloatingEmoji('💛');
    });
    
    // ========== FLOATING EMOJIS ==========
    function createFloatingEmoji(emojiType = null) {
        const emojisList = ['🌸', '🍒', '🧸', '🎀', '✨', '🍰', '💛', '🐻‍❄️', '🍬', '🎉', '🙌', '📸', '🐱', '🎁'];
        const chosen = emojiType || emojisList[Math.floor(Math.random() * emojisList.length)];
        const floatingDiv = document.createElement('div');
        floatingDiv.classList.add('floating-emoji');
        floatingDiv.innerHTML = chosen;
        floatingDiv.style.left = Math.random() * 90 + 5 + '%';
        floatingDiv.style.bottom = '-20px';
        floatingDiv.style.fontSize = (Math.random() * 1.5 + 1.2) + 'rem';
        document.body.appendChild(floatingDiv);
        setTimeout(() => floatingDiv.remove(), 2800);
    }
    
    // auto floating emojis for extra cuteness
    setInterval(() => {
        if (Math.random() > 0.7) createFloatingEmoji();
    }, 3000);
    
    // initial floating joy on load
    window.addEventListener('load', () => {
        for (let i = 0; i < 6; i++) {
            setTimeout(() => createFloatingEmoji('🎀'), i * 200);
        }
    });
    
    // Add hover sparkle effect on polaroids
    const style = document.createElement('style');
    style.textContent = `
        .polaroid {
            transition: all 0.25s ease;
        }
        .compliment-badge {
            transition: all 0.2s;
        }
    `;
    document.head.appendChild(style);
    
    // Also add a little instruction tooltip
    const galleryTitle = document.querySelector('.gallery-title');
    if (galleryTitle) {
        galleryTitle.style.cursor = 'default';
    }
</script>
</body>
</html>
