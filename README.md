# lab02-debugging

# Setup 

Create a [Shadertoy account](https://www.shadertoy.com/). Either fork this shadertoy, or create a new shadertoy and copy the code from the [Debugging Puzzle](https://www.shadertoy.com/view/flGfRc).

Let's practice debugging! We have a broken shader. It should produce output that looks like this:
[Unbelievably beautiful shader](https://user-images.githubusercontent.com/1758825/200729570-8e10a37a-345d-4aff-8eff-6baf54a32a40.webm)

It don't do that. Correct THREE of the FIVE bugs that are messing up the output. You are STRONGLY ENCOURAGED to work with a partner and pair program to force you to talk about your debugging thought process out loud.

Extra credit if you can find all FIVE bugs.

# Debugs
1) In mainImage() we never call uv2 so I just replaced 'vec uv2 = ...' with 'uv = ...' to fix the black screen.
2) In raycast(), we horizontal scale is messed up as it was 'iResolution.x / iResolution.x' which I fixed with 'iResolution.x / iResolution.y' which is the correct horizontal screen ratio.
3) In sdf3d(), to apply specular, we need to replace 'dir = reflect(eye, nor);' with 'dir = reflect(dir, nor);'.
4) In march(), to fix the floor not extending out as far as we want, change the value that i goes till. I replaced 'i < 64' with 'i < 200'. This also gets rid of the weird warping around the spheres.
5) 

Partner: Marcus \n
Shadertoy: https://www.shadertoy.com/view/wcsfWf

# Submission
- Create a pull request to this repository
- In the README, include the names of both your team members
- In the README, create a link to your shader toy solution with the bugs corrected
- In the README, describe each bug you found and include a sentence about HOW you found it.
- Make sure all three of your shadertoys are set to UNLISTED or PUBLIC (so we can see them!)
