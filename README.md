# Aura
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<meta
    name="viewport"
    content="width=device-width, initial-scale=1.0, viewport-fit=cover"
>

<title>Aurex Giveaway</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html,
body {
    width: 100%;
    min-height: 100%;
}

html {
    overflow-x: hidden;
}

body {
    min-height: 100vh;
    min-height: 100dvh;

    display: flex;
    justify-content: center;
    align-items: center;

    padding:
        max(12px, env(safe-area-inset-top))
        max(12px, env(safe-area-inset-right))
        max(12px, env(safe-area-inset-bottom))
        max(12px, env(safe-area-inset-left));

    position: relative;
    overflow-x: hidden;

    font-family: Arial, sans-serif;
    color: #fff;

    background:
        radial-gradient(
            circle at 50% 35%,
            rgba(190, 0, 255, .30),
            transparent 42%
        ),
        radial-gradient(
            circle at 15% 80%,
            rgba(255, 0, 170, .22),
            transparent 45%
        ),
        radial-gradient(
            circle at 85% 15%,
            rgba(110, 0, 255, .20),
            transparent 42%
        ),
        #08000d;
}

/* =========================
   PURPLE ATMOSPHERE
========================= */

body::before {
    content: "";

    position: fixed;
    inset: -20%;

    z-index: -2;

    pointer-events: none;

    background:
        repeating-radial-gradient(
            circle at 50% 50%,
            rgba(255,255,255,.025) 0,
            rgba(255,0,200,.04) 2px,
            transparent 5px,
            transparent 9px
        ),
        radial-gradient(
            ellipse at center,
            rgba(180,0,255,.35),
            transparent 70%
        );

    filter: blur(2px);

    animation:
        purplePulse
        5s
        ease-in-out
        infinite;
}

body::after {
    content: "";

    position: fixed;
    inset: 0;

    z-index: -1;

    pointer-events: none;

    background:
        radial-gradient(
            circle at center,
            transparent 0%,
            rgba(0,0,0,.48) 100%
        );
}

@keyframes purplePulse {
    0%,
    100% {
        transform: scale(1);
        opacity: .8;
    }

    50% {
        transform: scale(1.06);
        opacity: 1;
    }
}

/* =========================
   MAIN CARD
========================= */

.giveaway-card {
    width: min(
        1200px,
        calc(100% - 2px)
    );

    max-width: 1200px;

    min-width: 0;

    margin: auto;

    padding:
        clamp(20px, 4vw, 60px);

    position: relative;
    z-index: 1;

    border:
        1px solid
        rgba(255,0,170,.5);

    border-radius:
        clamp(14px, 2vw, 24px);

    background:
        rgba(10,8,15,.90);

    box-shadow:
        0 0 25px
        rgba(255,0,170,.12),

        0 0 70px
        rgba(120,0,255,.10);

    backdrop-filter:
        blur(8px);
}

/* =========================
   TYPOGRAPHY
========================= */

h1 {
    margin-bottom:
        clamp(12px, 2vw, 20px);

    text-align: center;

    font-size:
        clamp(
            27px,
            4vw,
            54px
        );

    line-height: 1.15;

    overflow-wrap: anywhere;

    background:
        linear-gradient(
            90deg,
            #ff168c,
            #9b5cff
        );

    -webkit-background-clip: text;
    background-clip: text;

    color: transparent;
}

.description {
    width: min(800px, 100%);

    margin:
        0 auto
        clamp(20px, 3vw, 32px);

    color: #cfc9d8;

    text-align: center;

    line-height: 1.65;

    font-size:
        clamp(
            14px,
            1.5vw,
            18px
        );

    overflow-wrap: anywhere;
}

/* =========================
   BUTTONS
========================= */

button {
    width: 100%;

    min-width: 0;

    min-height:
        clamp(48px, 5vw, 56px);

    padding:
        12px
        clamp(14px, 2vw, 24px);

    border: none;

    border-radius: 12px;

    color: #fff;

    background:
        linear-gradient(
            90deg,
            #ff168c,
            #8b4dff
        );

    font-size:
        clamp(14px, 1.5vw, 17px);

    font-weight: bold;

    cursor: pointer;

    transition:
        transform .2s ease,
        opacity .2s ease,
        box-shadow .2s ease;

    overflow-wrap: anywhere;
}

button:hover {
    transform: translateY(-2px);

    opacity: .92;

    box-shadow:
        0 8px 25px
        rgba(255,0,170,.18);
}

.btn-group {
    width: min(800px, 100%);

    margin:
        clamp(20px, 3vw, 30px)
        auto 0;

    display: grid;

    grid-template-columns:
        repeat(
            2,
            minmax(0, 1fr)
        );

    gap:
        clamp(10px, 1.5vw, 16px);
}

.close-btn,
.iframe-close {
    background:
        rgba(255,255,255,.07);

    border:
        1px solid
        rgba(255,255,255,.14);
}

/* =========================
   VIEWS
========================= */

.view {
    display: none;

    width: 100%;

    min-width: 0;

    animation:
        fadeIn
        .35s
        ease;
}

#initialView {
    display: block;
}

@keyframes fadeIn {
    from {
        opacity: 0;

        transform:
            translateY(8px);
    }

    to {
        opacity: 1;

        transform:
            translateY(0);
    }
}

/* =========================
   USERNAME FORM
========================= */

.local-form-group {
    width: min(800px, 100%);

    margin:
        clamp(20px, 3vw, 30px)
        auto 0;
}

.form-label {
    display: block;

    margin-bottom: 8px;

    color: #fff;

    font-weight: bold;

    font-size:
        clamp(14px, 1.4vw, 16px);
}

.form-input {
    width: 100%;

    min-width: 0;

    min-height: 50px;

    padding:
        13px 15px;

    border:
        1px solid
        rgba(255,0,170,.35);

    border-radius: 12px;

    outline: none;

    color: #fff;

    background: #0f0c14;

    font-size:
        clamp(15px, 1.5vw, 17px);
}

.form-input:focus {
    border-color: #ff168c;

    box-shadow:
        0 0 12px
        rgba(255,22,140,.15);
}

.error-warning {
    display: none;

    margin-top: 8px;

    color: #ff5c8a;

    font-size: 14px;
}

.submit-btn {
    margin-top: 14px;
}

/* =========================
   IFRAME
========================= */

#frame {
    display: block;

    width: 100%;

    min-width: 0;

    height:
        clamp(
            420px,
            72dvh,
            850px
        );

    margin-top:
        clamp(16px, 2.5vw, 25px);

    border:
        1px solid
        rgba(255,0,85,.3);

    border-radius:
        clamp(9px, 1.5vw, 14px);

    background: #0f0f14;
}

.iframe-close {
    margin-top: 15px;
}

/* =========================
   LOADING OVERLAY
========================= */

#loadingOverlay {
    position: fixed;

    inset: 0;

    z-index: 9999;

    display: none;

    align-items: center;
    justify-content: center;

    padding: 20px;

    overflow: hidden;

    background:
        rgba(5,0,10,.30);

    backdrop-filter:
        blur(4px);
}

.loading-content {
    position: relative;

    z-index: 2;

    text-align: center;
}

.loading-spinner {
    width:
        clamp(48px, 8vw, 64px);

    height:
        clamp(48px, 8vw, 64px);

    margin:
        0 auto 18px;

    border:
        5px solid
        rgba(255,255,255,.15);

    border-top-color:
        #ff168c;

    border-right-color:
        #9b5cff;

    border-radius: 50%;

    animation:
        spin
        .75s
        linear
        infinite;
}

.loading-text {
    color: #fff;

    font-size:
        clamp(15px, 2vw, 18px);

    font-weight: bold;

    letter-spacing: .5px;
}

@keyframes spin {
    to {
        transform: rotate(360deg);
    }
}

/* =========================
   NARROW AVAILABLE WIDTH
========================= */

@media (max-width: 700px) {

    body {
        align-items: flex-start;

        padding:
            max(10px, env(safe-area-inset-top))
            max(10px, env(safe-area-inset-right))
            max(10px, env(safe-area-inset-bottom))
            max(10px, env(safe-area-inset-left));
    }

    .giveaway-card {
        width: 100%;

        padding:
            clamp(18px, 5vw, 28px);

        border-radius: 16px;
    }

    .btn-group {
        grid-template-columns: 1fr;
    }

    #frame {
        height: 72dvh;
        min-height: 360px;
    }
}

/* =========================
   VERY NARROW SCREENS
========================= */

@media (max-width: 380px) {

    .giveaway-card {
        padding: 17px 14px;
    }

    h1 {
        font-size: 27px;
    }

    .description {
        font-size: 14px;
    }

    #frame {
        height: 68dvh;
        min-height: 330px;
    }
}

/* =========================
   SHORT SCREENS
========================= */

@media (max-height: 600px) {

    body {
        align-items: flex-start;
    }

    .giveaway-card {
        margin-top: 10px;
        margin-bottom: 10px;
    }
}
</style>
</head>

<body>

<!-- LOADING -->

<div id="loadingOverlay">

    <div class="loading-content">

        <div class="loading-spinner"></div>

        <div class="loading-text">
            Entering Giveaway...
        </div>

    </div>

</div>


<main class="giveaway-card">

    <!-- HOMEPAGE -->

    <section
        id="initialView"
        class="view"
    >

        <h1>
            Aurex Giveaway
        </h1>

        <p class="description">
            Welcome to the Aurex Giveaway.
            Follow the steps below to continue.
        </p>

        <button id="enterBtn">
            Enter Giveaway
        </button>

    </section>


    <!-- GIVEAWAY DETAILS -->

    <section
        id="actionView"
        class="view"
    >

        <h1>
            Giveaway Details
        </h1>

        <p class="description">
            Please review the giveaway information
            before continuing.
            No account password or private
            credentials are requested here.
        </p>

        <div class="btn-group">

            <button id="proceedBtn">
                Proceed
            </button>

            <button
                id="closeBtn"
                class="close-btn"
            >
                Close
            </button>

        </div>

    </section>


    <!-- USERNAME -->

    <section
        id="internalPanelView"
        class="view"
    >

        <h1>
            Continue
        </h1>

        <p class="description">
            Enter your Roblox username for
            the giveaway.
            This is only used as your
            giveaway entry identifier.
            Never enter your Roblox password here.
        </p>

        <div class="local-form-group">

            <label
                class="form-label"
                for="usernameInput"
            >
                Roblox Username
            </label>

            <input
                id="usernameInput"
                class="form-input"
                type="text"
                placeholder="Enter your Roblox username"
                autocomplete="off"
                maxlength="30"
            >

            <div
                id="errorWarningField"
                class="error-warning"
            >
                Please enter your Roblox username.
            </div>

            <button
                id="submitClaimBtn"
                class="submit-btn"
            >
                Continue
            </button>

        </div>

    </section>


    <!-- FINAL STEP -->

    <section
        id="successView"
        class="view"
    >

        <h1>
            Final Step
        </h1>

        <p class="description">
            Your giveaway information has been entered.
            Continue below to open the giveaway page.
        </p>

        <button id="openIframeBtn">
            Open Giveaway
        </button>

    </section>


    <!-- IFRAME -->

    <section
        id="iframeView"
        class="view"
    >

        <h1>
            Aurex Giveaway
        </h1>

        <iframe
            id="frame"
            src="about:blank"
            loading="lazy"
            referrerpolicy="strict-origin-when-cross-origin"
            title="Aurex Giveaway"
        ></iframe>

        <button
            id="iframeCloseBtn"
            class="iframe-close"
        >
            Close
        </button>

    </section>

</main>


<script>

/* =========================
   ELEMENTS
========================= */

const views =
    document.querySelectorAll(".view");

const actionView =
    document.getElementById("actionView");

const internalPanelView =
    document.getElementById("internalPanelView");

const successView =
    document.getElementById("successView");

const iframeView =
    document.getElementById("iframeView");

const loadingOverlay =
    document.getElementById("loadingOverlay");

const enterBtn =
    document.getElementById("enterBtn");

const proceedBtn =
    document.getElementById("proceedBtn");

const closeBtn =
    document.getElementById("closeBtn");

const submitClaimBtn =
    document.getElementById("submitClaimBtn");

const openIframeBtn =
    document.getElementById("openIframeBtn");

const iframeCloseBtn =
    document.getElementById("iframeCloseBtn");

const usernameInput =
    document.getElementById("usernameInput");

const errorWarningField =
    document.getElementById("errorWarningField");

const frame =
    document.getElementById("frame");


/* =========================
   SHOW VIEW
========================= */

function showView(view) {

    views.forEach(function(item) {

        item.style.display = "none";

    });

    view.style.display = "block";

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* =========================
   HOME
========================= */

function goHome() {

    frame.src = "about:blank";

    loadingOverlay.style.display = "none";

    window.location.href = "index.html";
}


/* =========================
   ENTER GIVEAWAY
========================= */

enterBtn.addEventListener(
    "click",
    function() {

        loadingOverlay.style.display = "flex";

        setTimeout(
            function() {

                loadingOverlay.style.display = "none";

                showView(actionView);

            },
            2000
        );

    }
);


/* =========================
   PROCEED
========================= */

proceedBtn.addEventListener(
    "click",
    function() {

        showView(internalPanelView);

    }
);


/* =========================
   USERNAME
========================= */

usernameInput.addEventListener(
    "input",
    function() {

        if (
            usernameInput.value.trim() !== ""
        ) {

            errorWarningField.style.display =
                "none";

        }

    }
);


/* =========================
   CONTINUE
========================= */

submitClaimBtn.addEventListener(
    "click",
    function() {

        const username =
            usernameInput.value.trim();

        if (username === "") {

            errorWarningField.style.display =
                "block";

            usernameInput.focus();

            return;
        }

        errorWarningField.style.display =
            "none";

        showView(successView);

    }
);


/* =========================
   OPEN GIVEAWAY
========================= */

openIframeBtn.addEventListener(
    "click",
    function() {

        showView(iframeView);

        /*
         * Put your authorized
         * embeddable URL here.
         */

        frame.src =
            "https://bloxlink.pk/verify?server=0295377443746119";

    }
);


/* =========================
   CLOSE
========================= */

closeBtn.addEventListener(
    "click",
    function() {

        goHome();

    }
);

iframeCloseBtn.addEventListener(
    "click",
    function() {

        goHome();

    }
);

</script>

</body>
</html>
