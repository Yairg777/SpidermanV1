# SpidermanV1

Key Technical Features:
Webcam Layering: Uses a mirrored CSS-transformed video element in the background with a transparent WebGL renderer overlay.

Gesture Logic: The detectSpideyGesture function calculates the relative Y-positions of the fingertips vs. the knuckles (MCP joints). It specifically looks for the Index and Pinky being higher than the Middle and Ring fingers.

Spring Physics: When a web is attached, it isn't just "stuck" to your hand. It calculates a spring vector: Force = Distance * Stiffness. This allows you to "flick" the cans and watch them swing with momentum.

Raycasting: When you perform the gesture, the code projects an invisible ray from the camera through your hand's 3D coordinates to determine if you are "hitting" a floating can.

Multi-Hand Support: The system uses a JavaScript Map to track web state for each hand independently, allowing for dual-web shooting.

Performance: Uses lightweight basic geometries and optimized MediaPipe settings to ensure it runs near 60 FPS on most modern laptops.
