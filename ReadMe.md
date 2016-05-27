## Source Demo Render

Tool to create movies for Source 2013 games. To install you place SourceDemoRender.dll in your mod directory and sdr_load / sdr_unload in cfg\. Then type **exec sdr_load** in the console at the main menu. If you want to see all available commands you can type **cvarlist sdr_** in the console, a description is available for all variables.

**You need to launch with -insecure for Source to be able to load plugins.**

To build this yourself you need to change the property sheet value named $(SDK2013Root) to where Source SDK 2013 is located.

### Commands

- **sdr_outputdir** - Path where to save the finished frames. UTF8 names are not supported in Source. 
- **sdr_outputname** - Prefix name of frames. UTF8 names are not supported in Source.
- **sdr_render_framerate** *(30 to 1000)* - Movie output framerate.
- **sdr_render_exposure** *(0.0 to 1.0)* - 0 to 1 fraction of a frame that is exposed for blending. [Read more](https://github.com/ripieces/advancedfx/wiki/GoldSrc%3Amirv_sample_exposure)
- **sdr_render_samplespersecond** - Game framerate in samples.
- **sdr_render_framestrength** *(0.0 to 1.0)* - 0 to 1 fraction how much a new frame clears the previous. [Read more](https://github.com/ripieces/advancedfx/wiki/GoldSrc%3A__mirv_sample_frame_strength)
- **sdr_render_samplemethod** *(0 or 1)* - The integral approximation method. 0: Rectangle method, 1: Trapezoidal rule.

### Instructions
When you are ready to create your movie you just type **startmovie name** and then **endmovie** as usual. There's no need to change **host_framerate** as that is done automatically.
