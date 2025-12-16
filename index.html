<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Miniso World: Platinum Arcade</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@700;900&family=Fredoka+One&display=swap" rel="stylesheet">
    
    <script src='https://cdnjs.cloudflare.com/ajax/libs/three.js/r83/three.min.js'></script>
    <script src='https://cdnjs.cloudflare.com/ajax/libs/gsap/1.20.3/TweenMax.min.js'></script>

    <style>
        :root {
            --red: #E60012;
            --white: #ffffff;
            --gray: #f5f5f5;
            --text: #333;
            --gold: #FFD700;
        }

        body {
            margin: 0;
            overflow: hidden;
            font-family: 'Nunito', sans-serif;
            background-color: var(--gray);
            user-select: none;
            touch-action: none;
        }

        .hidden { display: none !important; }

        /* --- APP SHELL --- */
        .app-screen {
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 100%;
            display: flex;
            flex-direction: column;
            background: var(--gray);
        }

        /* HEADER */
        .app-header {
            background: var(--red);
            color: white;
            padding: 15px 20px;
            border-bottom-left-radius: 30px;
            border-bottom-right-radius: 30px;
            box-shadow: 0 5px 20px rgba(230,0,18,0.3);
            display: flex;
            flex-direction: column;
            gap: 10px;
            z-index: 10;
        }

        .logo-container { display: flex; justify-content: center; }
        
        .miniso-logo-text {
            font-family: 'Fredoka One', cursive;
            font-size: 28px;
            letter-spacing: 2px;
            border: 3px solid white;
            padding: 2px 10px;
            border-radius: 8px;
        }

        .user-bar { display: flex; justify-content: space-between; align-items: end; }

        .points-badge {
            background: white;
            color: var(--red);
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: 900;
            font-size: 20px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* MENU AREA */
        .scroll-area {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
            padding-bottom: 80px;
            -webkit-overflow-scrolling: touch;
        }

        .section-title {
            font-size: 18px;
            color: var(--text);
            margin: 25px 0 15px 0;
            font-weight: 900;
            letter-spacing: 1px;
        }

        /* GAME CARDS */
        .game-card {
            background: white;
            border-radius: 20px;
            margin-bottom: 20px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            position: relative;
            transition: transform 0.1s;
            cursor: pointer;
        }

        .game-card:active { transform: scale(0.98); }

        .game-thumb { height: 110px; position: relative; }
        .game-1-bg { background: linear-gradient(45deg, #ff9a9e, #fecfef); }
        .game-2-bg { background: linear-gradient(45deg, #a18cd1, #fbc2eb); }
        .game-3-bg { background: linear-gradient(45deg, #84fab0, #8fd3f4); }
        .game-4-bg { background: linear-gradient(45deg, #fddb92, #d1fdff); }
        .game-5-bg { background: linear-gradient(45deg, #cfd9df, #e2ebf0); }

        .game-icon-overlay {
            position: absolute;
            bottom: -15px;
            right: 20px;
            font-size: 50px;
            filter: drop-shadow(0 4px 8px rgba(0,0,0,0.2));
        }

        .card-content { padding: 15px 20px; padding-top: 25px; }
        .game-title { font-size: 20px; color: var(--text); font-weight: 800; font-family: 'Fredoka One', cursive; }
        .game-desc { font-size: 14px; color: #777; margin-bottom: 10px; }

        .play-btn {
            display: inline-block;
            background: var(--red);
            color: white;
            padding: 6px 20px;
            border-radius: 15px;
            font-size: 12px;
            font-weight: bold;
        }

        /* REWARDS */
        .rewards-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }

        .reward-card {
            background: white;
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .reward-icon { font-size: 30px; margin-bottom: 5px; }
        .reward-title { font-weight: 800; margin-bottom: 5px; font-size: 14px; }
        .reward-cost { font-size: 12px; color: #888; margin-bottom: 10px; }

        .redeem-btn {
            background: var(--text);
            color: white;
            border: none;
            padding: 8px 0;
            border-radius: 20px;
            font-weight: bold;
            font-size: 11px;
            width: 100%;
            cursor: pointer;
        }
        .redeem-btn.locked { background: #eee; color: #aaa; pointer-events: none; }

        /* GAME LAYERS */
        #game-layer { background: #222; }
        canvas { display: block; width: 100%; height: 100%; }
        #stacker-layer { background: #ffe6f2; position: absolute; top: 0; left: 0; width: 100%; height: 100%; }

        /* HUD & MODALS */
        .game-hud {
            position: absolute;
            top: 0; left: 0;
            width: 100%;
            padding: 20px;
            box-sizing: border-box;
            display: flex;
            justify-content: space-between;
            pointer-events: none;
            z-index: 50;
        }

        .hud-score {
            font-size: 50px;
            color: white;
            text-shadow: 2px 2px 0 var(--red);
            font-weight: 900;
            font-family: 'Fredoka One';
        }

        .exit-btn {
            pointer-events: auto;
            background: white;
            color: var(--red);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }

        .modal-overlay {
            position: absolute;
            top:0; left:0;
            width:100%; height:100%;
            background: rgba(0,0,0,0.85);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 100;
        }

        .modal-box {
            background: white;
            padding: 30px;
            border-radius: 25px;
            text-align: center;
            width: 85%;
            max-width: 320px;
            animation: popIn 0.3s;
        }

        .big-btn {
            background: var(--red);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 20px;
            border-radius: 30px;
            margin-top: 20px;
            width: 100%;
            font-weight: 900;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(230,0,18,0.4);
        }

        @keyframes popIn {
            from{transform:scale(0.8);opacity:0}
            to{transform:scale(1);opacity:1}
        }
    </style>
</head>
<body>

    <div id="home-screen" class="app-screen">
        <div class="app-header">
            <div class="logo-container"><div class="miniso-logo-text">MINISO</div></div>
            <div class="user-bar">
                <div>
                    <div style="font-size:12px; opacity:0.9;">WELCOME</div>
                    <div style="font-size:20px; font-weight: 900;">Super Member</div>
                </div>
                <div class="points-badge"><span>💎</span> <span id="global-points">100</span></div>
            </div>
        </div>
        
        <div class="scroll-area">
            <div class="section-title"><span>🎮</span> GAMES</div>
            
            <div class="game-card" onclick="App.launchGame('stacker')">
                <div class="game-thumb game-2-bg"><div class="game-icon-overlay">🗼</div></div>
                <div class="card-content">
                    <div class="game-title">Miniso Tower 3D</div>
                    <div class="game-desc">Stack blocks perfectly!</div>
                    <div class="play-btn">PLAY</div>
                </div>
            </div>

            <div class="game-card" onclick="App.launchGame('pacman')">
                <div class="game-thumb game-4-bg"><div class="game-icon-overlay">🟡</div></div>
                <div class="card-content">
                    <div class="game-title">Miniso Muncher</div>
                    <div class="game-desc">Eat dots! (Arrow Keys/Swipe)</div>
                    <div class="play-btn">PLAY</div>
                </div>
            </div>

            <div class="game-card" onclick="App.launchGame('snake')">
                <div class="game-thumb game-1-bg"><div class="game-icon-overlay">🐍</div></div>
                <div class="card-content">
                    <div class="game-title">Snake 3D</div>
                    <div class="game-desc">Collect gifts! (Arrow Keys/Swipe)</div>
                    <div class="play-btn">PLAY</div>
                </div>
            </div>

            <div class="game-card" onclick="App.launchGame('smasher')">
                <div class="game-thumb game-3-bg"><div class="game-icon-overlay">🔨</div></div>
                <div class="card-content">
                    <div class="game-title">Price Smasher</div>
                    <div class="game-desc">Click/Tap the Tags!</div>
                    <div class="play-btn">PLAY</div>
                </div>
            </div>

            <div class="game-card" onclick="App.launchGame('bounce')">
                <div class="game-thumb game-5-bg"><div class="game-icon-overlay">🎾</div></div>
                <div class="card-content">
                    <div class="game-title">Bounce</div>
                    <div class="game-desc">Break tiles. (Mouse/Touch)</div>
                    <div class="play-btn">PLAY</div>
                </div>
            </div>

            <div class="section-title"><span>🎁</span> REWARDS</div>
            <div class="rewards-grid">
                <div class="reward-card">
                    <div class="reward-icon">🎟️</div>
                    <div class="reward-title">5% Off</div>
                    <div class="reward-cost">100 Pts</div>
                    <button class="redeem-btn" data-cost="100">REDEEM</button>
                </div>
                <div class="reward-card">
                    <div class="reward-icon">🐧</div>
                    <div class="reward-title">Plushie</div>
                    <div class="reward-cost">500 Pts</div>
                    <button class="redeem-btn" data-cost="500">REDEEM</button>
                </div>
            </div>
        </div>
    </div>

    <div id="game-layer" class="app-screen hidden"><canvas id="gameCanvas"></canvas></div>
    <div id="stacker-layer" class="app-screen hidden"></div>

    <div id="hud-layer" class="game-hud hidden">
        <div class="exit-btn" onclick="App.exitGame()">✕</div>
        <div class="hud-score" id="game-score">0</div>
    </div>

    <div id="start-modal" class="modal-overlay hidden">
        <div class="modal-box">
            <h2 id="modal-title" style="margin:0; color:var(--red);">GAME</h2>
            <p id="modal-desc">Instructions</p>
            <button class="big-btn" onclick="App.startGameLoop()">START</button>
        </div>
    </div>

    <div id="end-modal" class="modal-overlay hidden">
        <div class="modal-box">
            <h2>GAME OVER</h2>
            <p>Points Earned:</p>
            <div style="font-size:60px; color:var(--gold); font-weight:900;">+<span id="earned-points">0</span></div>
            <button class="big-btn" onclick="App.exitGame()">COLLECT</button>
        </div>
    </div>

<script>
/**
 * SOUND SYSTEM (Synthesizer)
 * No external files needed.
 */
const SoundSys = {
    ctx: null,
    init: function() {
        if(!this.ctx) {
            this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
    },
    playTone: function(freq, type, duration, vol=0.1) {
        if(!this.ctx) return;
        if(this.ctx.state === 'suspended') this.ctx.resume();
        
        let osc = this.ctx.createOscillator();
        let gain = this.ctx.createGain();
        
        osc.type = type; // sine, square, sawtooth, triangle
        osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
        
        gain.gain.setValueAtTime(vol, this.ctx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.01, this.ctx.currentTime + duration);
        
        osc.connect(gain);
        gain.connect(this.ctx.destination);
        
        osc.start();
        osc.stop(this.ctx.currentTime + duration);
    },
    playTap: function() { this.playTone(600, 'sine', 0.1, 0.1); },
    playStack: function(combo) { 
        // Pitch gets higher with combo
        let pitch = 440 + (combo*50); 
        this.playTone(pitch, 'triangle', 0.15, 0.15); 
    },
    playScore: function() { 
        this.playTone(880, 'sine', 0.1, 0.1); 
        setTimeout(()=>this.playTone(1100, 'sine', 0.2, 0.1), 100);
    },
    playFail: function() { this.playTone(150, 'sawtooth', 0.5, 0.2); }
};

/**
 * MAIN APP CONTROLLER
 */
const App = {
    points: 100,
    activeGameId: null,
    canvas: document.getElementById('gameCanvas'),
    ctx: document.getElementById('gameCanvas').getContext('2d'),
    pendingScore: 0,

    init: function() {
        this.updateUI();
        this.resize();
        window.addEventListener('resize', ()=>this.resize());
        this.setupRedeem();
    },

    resize: function() {
        this.canvas.width = window.innerWidth;
        this.canvas.height = window.innerHeight;
        if(this.activeGameId && Game2D.active && Game2D.active.resize) {
            Game2D.active.resize(this.canvas.width, this.canvas.height);
        }
    },

    updateUI: function() {
        document.getElementById('global-points').innerText = this.points;
        document.querySelectorAll('.redeem-btn').forEach(b=>{
            let cost = parseInt(b.dataset.cost);
            if(this.points >= cost) {
                b.className = 'redeem-btn';
            } else {
                b.className = 'redeem-btn locked';
            }
        });
    },

    setupRedeem: function() {
        document.querySelectorAll('.redeem-btn').forEach(b => b.addEventListener('click', (e)=>{
            let cost = parseInt(e.target.dataset.cost);
            if(this.points >= cost) {
                SoundSys.playScore();
                this.points -= cost;
                alert("Redeemed successfully! Show this screen to cashier.");
                this.updateUI();
            }
        }));
    },

    launchGame: function(id) {
        SoundSys.init(); // Initialize audio context on user interaction
        SoundSys.playTap();
        
        this.activeGameId = id;
        document.getElementById('home-screen').classList.add('hidden');
        document.getElementById('start-modal').classList.remove('hidden');
        document.getElementById('end-modal').classList.add('hidden');
        document.getElementById('hud-layer').classList.remove('hidden');
        document.getElementById('game-score').innerText="0";

        let t="", d="";
        if(id==='stacker') {t="TOWER 3D"; d="Tap or Press Space to stack blocks.";}
        if(id==='pacman') {t="MUNCHER"; d="Swipe or Arrow Keys to move.";}
        if(id==='snake') {t="SNAKE 3D"; d="Swipe or Arrow Keys to turn.";}
        if(id==='smasher') {t="SMASHER"; d="Click/Tap the good tags!";}
        if(id==='bounce') {t="BOUNCE"; d="Drag mouse/finger to move paddle.";}

        document.getElementById('modal-title').innerText=t;
        document.getElementById('modal-desc').innerText=d;
    },

    startGameLoop: function() {
        SoundSys.playTap();
        document.getElementById('start-modal').classList.add('hidden');
        if(this.activeGameId==='stacker') {
            document.getElementById('stacker-layer').classList.remove('hidden');
            GameStacker.init();
        } else {
            document.getElementById('game-layer').classList.remove('hidden');
            Game2D.launch(this.activeGameId);
        }
    },

    finishGame: function(s) {
        // Prevent double finish calls
        if(!document.getElementById('hud-layer').classList.contains('hidden')){
            if(s > 0) SoundSys.playScore(); else SoundSys.playFail();
            document.getElementById('hud-layer').classList.add('hidden');
            document.getElementById('end-modal').classList.remove('hidden');
            document.getElementById('earned-points').innerText=s;
            this.pendingScore=s;
        }
    },

    exitGame: function() {
        SoundSys.playTap();
        if(this.activeGameId==='stacker') {
            GameStacker.stop();
            document.getElementById('stacker-layer').classList.add('hidden');
        } else {
            Game2D.stop();
            document.getElementById('game-layer').classList.add('hidden');
        }
        
        if(this.pendingScore) {
            this.points += this.pendingScore;
            this.pendingScore = 0;
        }

        document.getElementById('hud-layer').classList.add('hidden');
        document.getElementById('start-modal').classList.add('hidden');
        document.getElementById('end-modal').classList.add('hidden');
        document.getElementById('home-screen').classList.remove('hidden');
        
        this.activeGameId=null;
        this.updateUI();
    }
};

/**
 * 3D STACKER GAME (THREE.JS) - UPDATED LIGHTING & SOUND
 */
const GameStacker = {
    container: document.getElementById('stacker-layer'),
    scene:null, camera:null, renderer:null,
    blocks:[], activeBlock:null, state:'stopped', score:0,
    lightGroup: null, // To move lights with camera
    
    init: function() {
        this.score=0;
        document.getElementById('game-score').innerText=0;
        
        // Setup Three.js
        this.scene = new THREE.Scene();
        this.scene.background = new THREE.Color(0xffe6f2); // Miniso pink bg
        
        let aspect = window.innerWidth/window.innerHeight;
        this.camera = new THREE.OrthographicCamera(-20*aspect, 20*aspect, 20, -20, -100, 1000);
        this.camera.position.set(2,2,2);
        this.camera.lookAt(new THREE.Vector3(0,0,0));
        
        this.renderer = new THREE.WebGLRenderer({antialias:true, alpha:true});
        this.renderer.setSize(window.innerWidth, window.innerHeight);
        
        this.container.innerHTML='';
        this.container.appendChild(this.renderer.domElement);
        
        // --- NEW LIGHTING SETUP (PREVENTS DARKENING) ---
        // Hemisphere light comes from everywhere (Sky + Ground reflection)
        // Sky: White, Ground: Soft Pink
        const hemiLight = new THREE.HemisphereLight( 0xffffff, 0xffc0cb, 0.9 );
        this.scene.add( hemiLight );

        // Directional light for subtle shadows/depth (Sunlight)
        // We will move this light upward as the tower grows
        this.dirLight = new THREE.DirectionalLight(0xffffff, 0.5);
        this.dirLight.position.set(10, 20, 10);
        this.scene.add(this.dirLight);
        
        this.group = new THREE.Group();
        this.scene.add(this.group);
        
        this.blocks=[];
        // Base block
        this.addBlock({x:0,y:0,z:0,w:10,h:2,d:10,c:0xE60012});
        
        this.addActive();
        this.state='playing';
        this.animate();
        
        this.input = (e)=>{
            if(e.type==='keydown' && e.code!=='Space') return;
            e.preventDefault();
            if(this.state==='playing') this.place();
        };
        
        window.addEventListener('mousedown', this.input);
        window.addEventListener('touchstart', this.input);
        window.addEventListener('keydown', this.input);
    },
    
    stop: function() {
        this.state='stopped';
        window.removeEventListener('mousedown', this.input);
        window.removeEventListener('touchstart', this.input);
        window.removeEventListener('keydown', this.input);
        this.container.innerHTML = '';
    },
    
    addBlock: function(b) {
        // Use MeshPhongMaterial but relies on the strong Hemisphere light now
        let geo=new THREE.BoxGeometry(b.w,b.h,b.d);
        let mat=new THREE.MeshPhongMaterial({
            color:b.c, 
            flatShading: false, 
            shininess: 10
        });
        let mesh=new THREE.Mesh(geo,mat);
        mesh.position.set(b.x,b.y,b.z);
        this.group.add(mesh);
        this.blocks.push(b);
        return mesh;
    },
    
    addActive: function() {
        let p=this.blocks[this.blocks.length-1], idx=this.blocks.length, axis=idx%2===0?'x':'z';
        
        // Miniso Palette
        let colors = [0xE60012, 0xffffff, 0xffcad4, 0x81ecec];
        
        this.activeBlock={
            x:p.x, y:p.y+2, z:p.z,
            w:p.w, h:2, d:p.d,
            c:colors[idx%colors.length],
            axis:axis,
            dir:0.35,
            limit:15
        };
        this.activeBlock[axis]=-15;
        this.activeMesh=this.addBlock(this.activeBlock);
        this.blocks.pop(); 
    },
    
    place: function() {
        let a=this.activeBlock, p=this.blocks[this.blocks.length-1], ax=a.axis, dim=ax==='x'?'w':'d';
        let diff = a[ax] - p[ax];
        
        if(Math.abs(diff) > p[dim]) {
            this.state='ended';
            SoundSys.playFail(); // PLAY FAIL SOUND
            this.group.remove(this.activeMesh);
            setTimeout(()=>App.finishGame(this.score), 1000);
            return;
        }
        
        SoundSys.playStack(this.score % 5); // PLAY STACK SOUND
        
        let overlap = p[dim] - Math.abs(diff);
        a[dim] = overlap; 
        a[ax] -= diff/2; 
        
        this.group.remove(this.activeMesh);
        this.addBlock(a);
        
        this.score++;
        document.getElementById('game-score').innerText=this.score;
        
        // Move Camera AND Light Up
        TweenMax.to(this.camera.position, 0.5, {y:this.camera.position.y+2});
        TweenMax.to(this.dirLight.position, 0.5, {y:this.dirLight.position.y+2}); // Move sun up
        TweenMax.to(this.scene.position, 0.5, {y:this.scene.position.y-2});
        
        this.addActive();
    },
    
    animate: function() {
        if(this.state!=='playing') return;
        requestAnimationFrame(()=>this.animate());
        
        if(this.activeBlock) {
            let a=this.activeBlock;
            a[a.axis]+=a.dir;
            if(Math.abs(a[a.axis])>a.limit) a.dir*=-1;
            this.activeMesh.position[a.axis]=a[a.axis];
        }
        this.renderer.render(this.scene, this.camera);
    }
};

/**
 * 2D GAME ENGINE MANAGER
 */
const Game2D = {
    active: null,
    launch: function(id) {
        let w=window.innerWidth, h=window.innerHeight;
        App.canvas.width = w; App.canvas.height = h;
        
        if(id==='pacman') this.active = GamePacman;
        if(id==='snake') this.active = GameSnake;
        if(id==='smasher') this.active = GameSmasher;
        if(id==='bounce') this.active = GameBounce;
        
        this.active.init(w,h);
        this.loop();
    },
    stop: function() {
        if(this.active) this.active.stop();
        this.active=null;
    },
    loop: function() {
        if(!this.active) return;
        App.ctx.clearRect(0,0,App.canvas.width,App.canvas.height);
        this.active.update();
        this.active.draw(App.ctx);
        document.getElementById('game-score').innerText = this.active.score;
        
        if(this.active.isGameOver) App.finishGame(this.active.score);
        else requestAnimationFrame(()=>this.loop());
    }
};

/**
 * GAME: SMASHER
 */
const GameSmasher = {
    init: function(w,h) {
        this.w=w; this.h=h; this.score=0; this.isGameOver=false;
        this.grid=[];
        
        let sz=Math.min(w,h)/4;
        let sx=(w-(sz*3+20))/2, sy=(h-(sz*3+20))/2;
        
        for(let i=0;i<9;i++) {
            this.grid.push({
                x:sx+(i%3)*(sz+10),
                y:sy+Math.floor(i/3)*(sz+10),
                s:sz,
                st:'empty',
                tm:0
            });
        }
        
        this.input = (e) => {
            e.preventDefault();
            let r=App.canvas.getBoundingClientRect(), cx, cy;
            if(e.type==='mousedown') { cx=e.clientX-r.left; cy=e.clientY-r.top; }
            else { cx=e.touches[0].clientX-r.left; cy=e.touches[0].clientY-r.top; }
            
            this.grid.forEach(c=>{
                if(c.st!=='empty' && cx>c.x && cx<c.x+c.s && cy>c.y && cy<c.y+c.s) {
                    if(c.st==='bad') {
                        this.isGameOver=true;
                    }
                    else if(c.st==='good') { 
                        SoundSys.playTap(); // Sound
                        this.score+=10; c.st='hit'; c.tm=10; 
                    }
                }
            });
        };
        
        App.canvas.addEventListener('mousedown',this.input);
        App.canvas.addEventListener('touchstart',this.input);
    },
    stop: function() {
        App.canvas.removeEventListener('mousedown',this.input);
        App.canvas.removeEventListener('touchstart',this.input);
    },
    update: function() {
        if(Math.random()<0.03) {
            let e=this.grid.filter(c=>c.st==='empty');
            if(e.length) {
                let c=e[Math.floor(Math.random()*e.length)];
                c.st=Math.random()>0.3?'good':'bad';
                c.tm=60;
            }
        }
        this.grid.forEach(c=>{
            if(c.st!=='empty') {
                c.tm--;
                if(c.tm<=0) c.st='empty';
            }
        });
    },
    draw: function(c) {
        c.fillStyle="#e0f7fa"; c.fillRect(0,0,this.w,this.h);
        this.grid.forEach(g=>{
            c.fillStyle="#ccc";
            c.beginPath(); c.arc(g.x+g.s/2, g.y+g.s/2, g.s/2-5, 0, Math.PI*2); c.fill();
            
            if(g.st==='good') {
                c.fillStyle="#E60012"; c.fill();
                c.fillStyle="white"; c.font="30px Arial"; c.textAlign="center"; c.fillText("50%", g.x+g.s/2, g.y+g.s/2+10);
            }
            if(g.st==='bad') {
                c.fillStyle="#333"; c.fill();
                c.fillStyle="white"; c.font="30px Arial"; c.textAlign="center"; c.fillText("🐧", g.x+g.s/2, g.y+g.s/2+10);
            }
            if(g.st==='hit') {
                c.fillStyle="gold"; c.font="bold 20px Arial"; c.fillText("HIT!", g.x+g.s/2, g.y+g.s/2);
            }
        });
    }
};

/**
 * GAME: BOUNCE
 */
const GameBounce = {
    isPlaying: false, isGameOver: false, score: 0, width:0, height:0,
    paddle: {x:0, y:0, w:80, h:10},
    ball: {x:0, y:0, r:8, dx:4, dy:-4},
    bricks: [],
    
    init: function(w, h) {
        this.width=w; this.height=h; this.score=0; this.isGameOver=false;
        this.paddle = {x: w/2 - 40, y: h - 50, w: 80, h: 10};
        this.ball = {x: w/2, y: h - 70, r: 8, dx: 4, dy: -4};
        this.bricks = [];
        let rows=5, cols=6, pad=10;
        let bw=(w-(pad*(cols+1)))/cols;
        
        for(let r=0; r<rows; r++) 
            for(let c=0; c<cols; c++) 
                this.bricks.push({x:c*(bw+pad)+pad, y:r*30+50, w:bw, h:20, s:1});
        
        this.bindInput = (e) => {
            e.preventDefault();
            let x = e.touches?e.touches[0].clientX:e.clientX;
            this.paddle.x = Math.max(0, Math.min(this.width-this.paddle.w, x-this.paddle.w/2));
        };
        
        window.addEventListener('touchmove', this.bindInput, {passive:false});
        window.addEventListener('mousemove', this.bindInput);
        this.isPlaying = true;
    },
    stop: function() {
        this.isPlaying = false;
        window.removeEventListener('touchmove', this.bindInput);
        window.removeEventListener('mousemove', this.bindInput);
    },
    update: function() {
        if(this.isGameOver) return;
        this.ball.x+=this.ball.dx;
        this.ball.y+=this.ball.dy;
        
        if(this.ball.x<0 || this.ball.x>this.width) {
            this.ball.dx*=-1;
            SoundSys.playTap(); // Sound
        }
        if(this.ball.y<0) {
            this.ball.dy*=-1;
            SoundSys.playTap(); // Sound
        }
        if(this.ball.y>this.height) this.isGameOver=true;
        
        if(this.ball.y+this.ball.r > this.paddle.y && 
           this.ball.x>this.paddle.x && 
           this.ball.x<this.paddle.x+this.paddle.w) {
             this.ball.dy = -Math.abs(this.ball.dy);
             SoundSys.playTap(); // Sound
        }
        
        this.bricks.forEach(b => {
            if(b.s && this.ball.x>b.x && this.ball.x<b.x+b.w && this.ball.y>b.y && this.ball.y<b.y+b.h) {
                this.ball.dy*=-1;
                b.s=0;
                this.score+=10;
                SoundSys.playTap(); // Sound
            }
        });
    },
    draw: function(ctx) {
        ctx.fillStyle="#f0f8ff"; ctx.fillRect(0,0,this.width,this.height);
        ctx.fillStyle="#E60012"; ctx.fillRect(this.paddle.x, this.paddle.y, this.paddle.w, this.paddle.h);
        ctx.beginPath(); ctx.arc(this.ball.x, this.ball.y, this.ball.r, 0, Math.PI*2); ctx.fill();
        this.bricks.forEach(b => {
            if(b.s) { ctx.fillStyle="#ff9a9e"; ctx.fillRect(b.x, b.y, b.w, b.h); }
        });
    }
};

/**
 * GAME: SNAKE 3D
 */
const GameSnake = {
    isGameOver: false, score: 0, width: 0, height: 0, grid: 25,
    snake: [], dir: {x:1, y:0}, nextDir: {x:1, y:0}, food: {x:0, y:0},
    frameCount: 0, speed: 5, touchStartX: 0, touchStartY: 0,
    
    init: function(w, h) {
        this.width = w; this.height = h;
        this.score = 0; this.isGameOver = false;
        this.snake = [{x: 10, y: 10}, {x: 9, y: 10}, {x: 8, y: 10}];
        this.dir = {x: 1, y: 0}; this.nextDir = {x: 1, y: 0};
        this.placeFood();
        this.speed = 6; this.frameCount = 0;
        this.bindControls();
    },
    bindControls: function() {
        this.handleKey = (e) => {
            switch(e.key) {
                case 'ArrowUp': if(this.dir.y===0) this.nextDir = {x:0, y:-1}; break;
                case 'ArrowDown': if(this.dir.y===0) this.nextDir = {x:0, y:1}; break;
                case 'ArrowLeft': if(this.dir.x===0) this.nextDir = {x:-1, y:0}; break;
                case 'ArrowRight': if(this.dir.x===0) this.nextDir = {x:1, y:0}; break;
            }
        };
        this.handleTouchStart = (e) => {
            this.touchStartX = e.changedTouches[0].screenX;
            this.touchStartY = e.changedTouches[0].screenY;
        };
        this.handleTouchEnd = (e) => {
            let dx = e.changedTouches[0].screenX - this.touchStartX;
            let dy = e.changedTouches[0].screenY - this.touchStartY;
            if(Math.abs(dx) > Math.abs(dy) && Math.abs(dx) > 30) {
                if(dx > 0 && this.dir.x === 0) this.nextDir = {x:1, y:0};
                else if(dx < 0 && this.dir.x === 0) this.nextDir = {x:-1, y:0};
            } else if(Math.abs(dy) > 30) {
                if(dy > 0 && this.dir.y === 0) this.nextDir = {x:0, y:1};
                else if(dy < 0 && this.dir.y === 0) this.nextDir = {x:0, y:-1};
            }
        };
        window.addEventListener('keydown', this.handleKey);
        window.addEventListener('touchstart', this.handleTouchStart, {passive: false});
        window.addEventListener('touchend', this.handleTouchEnd, {passive: false});
    },
    stop: function() {
        window.removeEventListener('keydown', this.handleKey);
        window.removeEventListener('touchstart', this.handleTouchStart);
        window.removeEventListener('touchend', this.handleTouchEnd);
    },
    placeFood: function() {
        let cols = Math.floor(this.width / this.grid);
        let rows = Math.floor(this.height / this.grid);
        this.food = { 
            x: Math.floor(Math.random() * (cols-2)) + 1, 
            y: Math.floor(Math.random() * (rows-4)) + 2 
        };
    },
    update: function() {
        this.frameCount++;
        if(this.frameCount < this.speed) return;
        this.frameCount = 0;
        this.dir = this.nextDir;
        let head = {x: this.snake[0].x + this.dir.x, y: this.snake[0].y + this.dir.y};
        let cols = Math.floor(this.width / this.grid);
        let rows = Math.floor(this.height / this.grid);
        
        if(head.x < 0 || head.x >= cols || head.y < 0 || head.y >= rows || this.snake.some(s => s.x === head.x && s.y === head.y)) {
            this.isGameOver = true;
            return;
        }
        this.snake.unshift(head);
        if(head.x === this.food.x && head.y === this.food.y) {
            this.score += 10;
            SoundSys.playTap(); // Sound
            this.placeFood();
            if(this.speed > 3) this.speed -= 0.1;
        } else {
            this.snake.pop();
        }
    },
    draw: function(ctx) {
        ctx.fillStyle = "#fff0f5"; ctx.fillRect(0,0,this.width, this.height);
        this.drawIsometricGift(ctx, this.food.x * this.grid, this.food.y * this.grid, this.grid);
        this.snake.forEach((seg, i) => {
            ctx.fillStyle = i === 0 ? "#E60012" : "#ff9a9e";
            ctx.beginPath(); 
            if (ctx.roundRect) ctx.roundRect(seg.x*this.grid+1, seg.y*this.grid+1, this.grid-2, this.grid-2, 8);
            else ctx.rect(seg.x*this.grid+1, seg.y*this.grid+1, this.grid-2, this.grid-2);
            ctx.fill();
        });
    },
    drawIsometricGift: function(ctx, x, y, size) {
        let h = size * 0.8, w = size, d = size * 0.4;
        ctx.save(); ctx.translate(x + w/2, y + h/2);
        // Top
        ctx.fillStyle = "#E60012"; ctx.beginPath(); ctx.moveTo(0, -h/2); ctx.lineTo(w/2, -h/2 - d/2); ctx.lineTo(0, -h/2 - d); ctx.lineTo(-w/2, -h/2 - d/2); ctx.closePath(); ctx.fill();
        // Front
        ctx.fillStyle = "#ff4d4d"; ctx.beginPath(); ctx.moveTo(-w/2, -h/2 - d/2); ctx.lineTo(0, -h/2); ctx.lineTo(0, h/2); ctx.lineTo(-w/2, h/2 - d/2); ctx.closePath(); ctx.fill();
        // Side
        ctx.fillStyle = "#cc0000"; ctx.beginPath(); ctx.moveTo(0, -h/2); ctx.lineTo(w/2, -h/2 - d/2); ctx.lineTo(w/2, h/2 - d/2); ctx.lineTo(0, h/2); ctx.closePath(); ctx.fill();
        // Ribbon
        ctx.fillStyle = "#FFD700"; ctx.fillRect(-w/2, -h/2 - d/2 + h/2 - 2, w/2, 4); ctx.fillRect(0, -h/2 + h/2 - 2, w/2, 4);
        ctx.restore();
    }
};

/**
 * GAME: MINISO MUNCHER (PACMAN)
 */
const GamePacman = {
    isGameOver: false, score: 0, width: 0, height: 0, gridSize: 20, map: [], rows: 15, cols: 15,
    player: {x:1, y:1, pixelX:0, pixelY:0, dir:{x:0,y:0}, nextDir:{x:0,y:0}, speed: 4},
    ghosts: [], powerModeTimer: 0, touchStartX:0, touchStartY:0,
    baseMap: [
        [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
        [0,1,1,1,0,1,1,1,1,1,0,1,1,1,0],
        [0,1,0,1,0,1,0,0,0,1,0,1,0,1,0],
        [0,2,0,1,1,1,1,0,1,1,1,1,0,2,0],
        [0,1,0,0,0,1,0,0,0,1,0,0,0,1,0],
        [0,1,1,1,1,1,1,1,1,1,1,1,1,1,0],
        [0,0,0,1,0,0,0,3,0,0,0,1,0,0,0],
        [0,1,1,1,1,1,3,3,3,1,1,1,1,1,0],
        [0,0,0,1,0,0,0,0,0,0,0,1,0,0,0],
        [0,1,1,1,1,1,1,0,1,1,1,1,1,1,0],
        [0,1,0,0,0,1,0,0,0,1,0,0,0,1,0],
        [0,2,1,1,0,1,1,0,1,1,0,1,1,2,0],
        [0,0,0,1,0,1,0,0,0,1,0,1,0,0,0],
        [0,1,1,1,1,1,1,0,1,1,1,1,1,1,0],
        [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
    ],
    init: function(w, h) {
        this.width = w; this.height = h; this.score = 0; this.isGameOver = false; this.powerModeTimer = 0;
        this.map = JSON.parse(JSON.stringify(this.baseMap));
        this.gridSize = Math.floor(Math.min(w, h) / this.cols);
        this.offsetX = (w - (this.cols * this.gridSize)) / 2;
        this.offsetY = (h - (this.rows * this.gridSize)) / 2;
        
        this.player = {x:7, y:13, pixelX:0, pixelY:0, dir:{x:0,y:0}, nextDir:{x:0,y:0}, speed: this.gridSize/5};
        this.snapToGrid(this.player);
        
        this.ghosts = [
            {x:7, y:7, color:'red', dir:{x:1,y:0}, speed: this.gridSize/10, edible: false},
            {x:7, y:7, color:'pink', dir:{x:-1,y:0}, speed: this.gridSize/10, edible: false}
        ];
        this.ghosts.forEach(g => this.snapToGrid(g));
        this.bindControls();
    },
    stop: function() { this.unbindControls(); },
    resize: function(w, h) { this.init(w, h); },
    snapToGrid: function(actor) { actor.pixelX = actor.x * this.gridSize; actor.pixelY = actor.y * this.gridSize; },
    bindControls: function() {
        this.handleKey = (e) => {
            e.preventDefault();
            switch(e.key) {
                case 'ArrowUp': this.player.nextDir = {x:0, y:-1}; break;
                case 'ArrowDown': this.player.nextDir = {x:0, y:1}; break;
                case 'ArrowLeft': this.player.nextDir = {x:-1, y:0}; break;
                case 'ArrowRight': this.player.nextDir = {x:1, y:0}; break;
            }
        };
        this.handleTouchStart = (e) => {
            this.touchStartX = e.changedTouches[0].screenX;
            this.touchStartY = e.changedTouches[0].screenY;
        };
        this.handleTouchEnd = (e) => {
            let dx = e.changedTouches[0].screenX - this.touchStartX;
            let dy = e.changedTouches[0].screenY - this.touchStartY;
            if(Math.abs(dx) > Math.abs(dy) && Math.abs(dx) > 20) this.player.nextDir = dx > 0 ? {x:1, y:0} : {x:-1, y:0};
            else if(Math.abs(dy) > 20) this.player.nextDir = dy > 0 ? {x:0, y:1} : {x:0, y:-1};
        };
        window.addEventListener('keydown', this.handleKey);
        window.addEventListener('touchstart', this.handleTouchStart, {passive:false});
        window.addEventListener('touchend', this.handleTouchEnd, {passive:false});
    },
    unbindControls: function() {
        window.removeEventListener('keydown', this.handleKey);
        window.removeEventListener('touchstart', this.handleTouchStart);
        window.removeEventListener('touchend', this.handleTouchEnd);
    },
    update: function() {
        if(this.powerModeTimer > 0) this.powerModeTimer--;
        this.moveActor(this.player, true);
        
        let cell = this.map[this.player.y][this.player.x];
        if(cell === 1) { 
            this.map[this.player.y][this.player.x] = 3; this.score += 10; 
            if(this.score%20===0) SoundSys.playTap();
        }
        else if(cell === 2) { 
            this.map[this.player.y][this.player.x] = 3; this.score += 50; this.powerModeTimer = 300; 
            SoundSys.playTap();
        }
        if(this.score >= 1780) this.isGameOver = true;

        this.ghosts.forEach(g => {
            g.edible = this.powerModeTimer > 0;
            this.moveActor(g, false);
            if(Math.hypot(g.pixelX - this.player.pixelX, g.pixelY - this.player.pixelY) < this.gridSize/2) {
                if(g.edible) { this.score += 200; g.x=7; g.y=7; this.snapToGrid(g); SoundSys.playScore(); }
                else { this.isGameOver = true; }
            }
        });
    },
    moveActor: function(actor, isPlayer) {
        let targetX = actor.x * this.gridSize;
        let targetY = actor.y * this.gridSize;
        if(actor.pixelX === targetX && actor.pixelY === targetY) {
            if(isPlayer && this.isValidMove(actor.x + actor.nextDir.x, actor.y + actor.nextDir.y)) actor.dir = actor.nextDir;
            if(!this.isValidMove(actor.x + actor.dir.x, actor.y + actor.dir.y)) {
                actor.dir = {x:0,y:0};
                if(!isPlayer) {
                    let dirs = [{x:0,y:-1},{x:0,y:1},{x:-1,y:0},{x:1,y:0}].filter(d => this.isValidMove(actor.x+d.x, actor.y+d.y));
                    if(dirs.length) actor.dir = dirs[Math.floor(Math.random()*dirs.length)];
                }
            }
            if(actor.dir.x !== 0 || actor.dir.y !== 0) { actor.x += actor.dir.x; actor.y += actor.dir.y; }
        }
        targetX = actor.x * this.gridSize; targetY = actor.y * this.gridSize;
        if(actor.pixelX < targetX) actor.pixelX = Math.min(targetX, actor.pixelX + actor.speed);
        if(actor.pixelX > targetX) actor.pixelX = Math.max(targetX, actor.pixelX - actor.speed);
        if(actor.pixelY < targetY) actor.pixelY = Math.min(targetY, actor.pixelY + actor.speed);
        if(actor.pixelY > targetY) actor.pixelY = Math.max(targetY, actor.pixelY - actor.speed);
    },
    isValidMove: function(x, y) { return x>=0 && x<this.cols && y>=0 && y<this.rows && this.map[y][x] !== 0; },
    draw: function(ctx) {
        ctx.fillStyle = "#222"; ctx.fillRect(0,0,this.width, this.height);
        ctx.save(); ctx.translate(this.offsetX, this.offsetY);
        for(let r=0; r<this.rows; r++) {
            for(let c=0; c<this.cols; c++) {
                let x = c*this.gridSize, y = r*this.gridSize, cell = this.map[r][c];
                if(cell===0) { ctx.fillStyle = "#555"; ctx.fillRect(x,y,this.gridSize,this.gridSize); ctx.strokeStyle="#333"; ctx.strokeRect(x,y,this.gridSize,this.gridSize); }
                else if(cell===1) { ctx.fillStyle = "#FFB6C1"; ctx.beginPath(); ctx.arc(x+this.gridSize/2, y+this.gridSize/2, 3, 0, Math.PI*2); ctx.fill(); }
                else if(cell===2) { ctx.fillStyle = "#FFB6C1"; ctx.beginPath(); ctx.arc(x+this.gridSize/2, y+this.gridSize/2, 7, 0, Math.PI*2); ctx.fill(); }
            }
        }
        ctx.fillStyle = "#FFD700"; ctx.beginPath();
        ctx.arc(this.player.pixelX+this.gridSize/2, this.player.pixelY+this.gridSize/2, this.gridSize/2-2, 0.2*Math.PI, 1.8*Math.PI);
        ctx.lineTo(this.player.pixelX+this.gridSize/2, this.player.pixelY+this.gridSize/2); ctx.fill();
        this.ghosts.forEach(g => {
            ctx.fillStyle = g.edible ? "#88f" : g.color;
            let gx = g.pixelX+1, gy = g.pixelY+1, gs = this.gridSize-2;
            ctx.beginPath(); ctx.arc(gx+gs/2, gy+gs/2-2, gs/2, Math.PI, 0); ctx.lineTo(gx+gs, gy+gs); ctx.lineTo(gx, gy+gs); ctx.fill();
        });
        ctx.restore();
    }
};

// Initialize App
window.addEventListener('DOMContentLoaded', () => {
    App.init();
});
</script>
</body>
</html>
