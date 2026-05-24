    body, html {
        width: 100%;
        height: 100%;
        overflow: hidden;
        background: radial-gradient(circle at center, #1a050d 0%, #050002 100%);
        font-family: 'Georgia', serif;
        perspective: 1200px; /* Activates 3D depth environment */
    }

    /* 3D Ambient Universe Layer */
    .universe-3d {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0; left: 0;
        transform-style: preserve-3d;
        z-index: 1;
        pointer-events: none;
    }

    /* 3D High Density Floating Elements */
    .aman-heart-3d {
        position: absolute;
        transform-style: preserve-3d;
        animation: float3D 9s infinite ease-in-out;
        opacity: 0;
    }

    /* CSS Rendered 3D Heart Structure */
    .heart-mesh {
        position: relative;
        width: 60px;
        height: 60px;
        transform-style: preserve-3d;
        transform: rotateX(20deg) rotateY(20deg);
    }
    .heart-side {
        position: absolute;
        width: 100%;
        height: 100%;
        background: rgba(231, 76, 60, 0.75);
        border-radius: 50% 50% 0 0;
        transform-style: preserve-3d;
        box-shadow: inset 0 0 15px rgba(255,255,255,0.6), 0 5px 20px rgba(0,0,0,0.4);
    }
    /* Mathematical offsets to create true 3D thick volume shape */
    .side-left {
        transform: rotate(-45deg);
        transform-origin: 0 100%;
        left: 30px;
    }
    .side-right {
        transform: rotate(45deg);
        transform-origin: 100% 100%;
        right: 30px;
    }
    
    /* Floating Text Engravings inside/around 3D elements */
    .engraved-text {
        position: absolute;
        width: 120px;
        text-align: center;
        left: -30px;
        top: 20px;
        font-size: 14px;
        font-weight: 900;
        color: #ffffff;
        text-shadow: 0 0 8px #ff4d6d, 0 0 15px #ffffff;
        font-family: 'Arial', sans-serif;
        transform: translateZ(25px); /* Pushes name outward in 3D Space */
    }

    /* Secondary Pure Text Density Strings */
    .aman-text-cloud {
        position: absolute;
        color: rgba(255, 182, 193, 0.45);
        font-weight: bold;
        font-family: 'Arial', sans-serif;
        text-shadow: 0 0 10px rgba(255, 77, 109, 0.3);
        animation: drift3D 14s infinite linear;
    }

    /* 3D Kinetic Animations */
    @keyframes float3D {
        0% { transform: translateY(105vh) translateX(0px) translateZ(-500px) rotateY(0deg); opacity: 0; }
        15% { opacity: 0.9; }
        85% { opacity: 0.9; }
        100% { transform: translateY(-15vh) translateX(100px) translateZ(300px) rotateY(360deg); opacity: 0; }
    }

    @keyframes drift3D {
        0% { transform: translateY(105vh) translateZ(-800px) rotateX(0deg); opacity: 0; }
        10% { opacity: 0.6; }
        90% { opacity: 0.6; }
        100% { transform: translateY(-15vh) translateZ(100px) rotateX(360deg); opacity: 0; }
    }

    /* Main Glassmorphism Presentation UI */
    .stage-container {
        position: relative;
        z-index: 10;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
    }

    .interactive-card {
        background: rgba(20, 5, 10, 0.65);
        border: 2px solid rgba(255, 77, 109, 0.3);
        backdrop-filter: blur(25px);
        -webkit-backdrop-filter: blur(25px);
        padding: 40px;
        border-radius: 30px;
        width: 90%;
        max-width: 550px;
        text-align: center;
        box-shadow: 0 30px 60px rgba(0, 0, 0, 0.8), inset 0 0 30px rgba(255, 77, 109, 0.1);
        transform: rotateX(5deg);
        animation: cardEntrance 1.5s ease-out;
    }

    @keyframes cardEntrance {
        0% { transform: scale(0.8) rotateX(25deg) translateY(50px); opacity: 0; }
        100% { transform: scale(1) rotateX(5deg) translateY(0); opacity: 1; }
    }

    /* Cinematic 3D Header Typography */
    h1 {
        font-size: 2.5rem;
        color: #ff4d6d;
        margin-bottom: 25px;
        text-shadow: 0 0 10px rgba(255,77,109,0.6), 0 0 20px rgba(255,77,109,0.3);
        letter-spacing: 2px;
    }

    /* Real-Time Love Letter Messenger Screen */
    .chat-display-screen {
        background: rgba(0, 0, 0, 0.4);
        border-radius: 15px;
        padding: 20px;
        min-height: 140px;
        margin-bottom: 30px;
        border: 1px solid rgba(255, 255, 255, 0.1);
        display: flex;
        align-items: center;
        justify-content: center;
    }

    #typed-message {
        font-size: 1.2rem;
        line-height: 1.7;
        color: #fff0f3;
        font-style: italic;
        text-shadow: 0 1px 4px rgba(0,0,0,0.5);
    }

    /* Formatted Response Buttons */
    .decision-vault {
        display: flex;
        justify-content: center;
        gap: 25px;
        position: relative;
        height: 55px;
    }

    .btn-core {
        padding: 0 40px;
        font-size: 1.2rem;
        font-weight: bold;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    #acceptBtn {
        background: linear-gradient(45deg, #ff4d6d, #ff758f);
        color: white;
        box-shadow: 0 8px 25px rgba(255, 77, 109, 0.5);
    }
    #acceptBtn:hover {
        transform: scale(1.15) translateY(-3px);
        box-shadow: 0 12px 30px rgba(255, 77, 109, 0.7);
    }

    #declineBtn {
        background: #2b2b2b;
        color: #888;
        position: absolute;
        box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
</style># Eman-jan
