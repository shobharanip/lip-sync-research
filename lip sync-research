Exploring Modalities in the Wav2lip Model: A Comprehensive Analysis
Goal: Explore Wav2lip applicability for the generation of lip-synced videos on 2D animations.

The implementation of Wav2lip can be found here.

In the implementation of Wav2lip, there are three models used to generate lip-synced 'deepfake' clips:

The discriminator
The face detection method (in this implementation, it is the sf3d model)
The Wav2lip model
Wav2lip can be used as a standalone method of video generation or combined with other AI models to improve results.

Here is an example of Wav2lip being used on a human video, to give an idea:

Before:

 trump.mp4 
After Wav2lip:

 trump_biden.mp4 
As you can see Wav2lip can be the basis of a convincing lip sync video.

Application on animated videos
Extrapolation the success of Wav2lip onto animated videos is an interesting concept.

Here is an example of Wav2lip being used on an animated video:

 wav2lip+gan_nobackgroundnoise.mp4 
There are artifacts and other anomolies that occur, but the concept is there.

Installation
I reccomend using this model on a machine that has a cuda enabled GPU for faster procesing.
I also reccomend using conda for clean installation. To install the wav2lip repo on your machine (if not using Monmouth's wav2lip installationn):

conda create -n wav2lip python=3.10
conda activate wav2lip
git clone https://github.com/davidkundrats/Wav2Lip.git
cd wav2lip
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
pip install -r requirements.txt
After getting the model installed, you will need to import the weights. They can be found here; underneath the heading "Getting the weights": https://github.com/Rudrabha/Wav2Lip.

You will need to import the weights for the model (wav2lip) and the discriminator (expert discriminator). Place them in this folder: /checkpoints/ You also will need the weights for the sf3d face detector and place them in this folder: /face_detection/detection/sfd/

Thats it! You should be ready to go.

Running the model
The interface for inferenecing is done through inference.py.

python inference.py --checkpoint_path </path/to/wav2lip.pth> --face </path/to/video.mp4> --audio </path/to/an-audio-source>
