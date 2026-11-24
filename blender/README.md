# Blender setup notes

Use Blender's GUI or run a setup script in the Scripting workspace.

## Render settings

- Resolution X: 1080
- Resolution Y: 1920
- Percentage: 100%
- Frame rate: 30
- Start frame: 1
- End frame: 840
- Export format: FFmpeg video
- Video codec: H.264
- Output pixel format: YUV420

## Camera

- Camera type: Perspective
- Focal length: 50 mm
- Position and rotation: keyframe throughout the reel
- Keep the character and important text in the safe vertical area

## Quality settings

- Render engine: Eevee for fast preview work
- Cycles for final photorealistic-style renders if the computer is powerful enough
- Use soft area lights
- Use ambient occlusion
- Use contact shadows
- Keep viewport and final render settings consistent

## Simple movement

For a static picture scene:

1. Add a camera to the scene.
2. Set frame 1 camera location and scale.
3. Set an end camera location and scale near frame 840.
4. Insert keyframes for both positions.
5. Use easing or Bézier interpolation.

Avoid rapid motion; the reference style works best with gentle pushes, pans, and character actions.
