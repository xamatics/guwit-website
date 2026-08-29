DROP YOUR REAL IMAGES IN THIS FOLDER
====================================

The site works without any of these — every visual is drawn in CSS/SVG.
Adding real files makes it stronger. Use these exact names:

  og-cover.png          1200 x 630   Social share card. Purple background,
                                     logo + "Guwit Technology Solutions".
  apple-touch-icon.png  180 x 180    Home-screen icon on iPhone/iPad.
  guwit-logo.png        transparent  Your supplied logo, if you want to use
                                     the bitmap instead of assets/logo.svg.

  gungbe-1.png          Play Store screenshot of Learn Gungbe (Apo Omi)
  gungbe-2.png          A second screenshot
  owa-chat.png          Screenshot of a real Owa WhatsApp order
  team.jpg              Photo of the team or the Badagry office

To swap a drawn mock-up for a real screenshot, replace the contents of the
<div class="shot"> block in work.html with:

  <img src="assets/img/gungbe-1.png" alt="The Learn Gungbe lesson list">
