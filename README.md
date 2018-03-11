<img src='https://raw.githubusercontent.com/takusui/Kat.ai/master/git/title-logo.png' height="80">

Kat.ai is a multi-platform chatbot that adapts while talking with you. This project aims to speed up the transition of AI into people's life by providing the user with ease of access. Kat will be able to run in any environment and, by using an adaptable sequence to sequence model, speak any language.

There are many posibilities when it comes to the customization:
* Add your own 3D or 2D models and backgrounds.
* User made themes.
* Add your own voice bank.
* Implement custom commands.
* Sculpt Kat's personality to match your own or make it the opposite.
* More to come.

## Brain structure
![](https://raw.githubusercontent.com/takusui/Kat.ai/master/git/brain.png)

This project will focus on mimicking the human brain using neural networks.

### Language comprehension
Kat.ai will use a minimally trained sequence-to-sequence model built in Tensorflow to answer your questions.

![](https://raw.githubusercontent.com/takusui/Kat.ai/0e74c223a9b6e5eae9f37110425379dd58e1f4e8/git/seq2seq.png)

The model will try to improve itself by asking questions about words that it hasn't encountered before or by searching their definition on the internet. If one is found, you will be asked to confirm if it is correct. Obviously, if you trust a source, you can make the bot learn without asking you. It will try to identify idioms on its own and add them to the database.

### Speech
I will use the deep generative model of raw audio waveforms made by DeepMind, WaveNet. Check their [website](https://deepmind.com/blog/wavenet-generative-model-raw-audio/) to see some [examples](https://storage.googleapis.com/deepmind-media/pixie/us-english/wavenet-1.wav).

### Hearing
For now, Mozzila's [DeepSpeech](https://github.com/mozilla/DeepSpeech) seems promising. 

### Image/object recognition
Tensorflow already has an [Object detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) which works perfectly for the objective of this project.

### Facial recognition
The first step is to choose a system between [OpenFace](https://github.com/cmusatyalab/openface) and [DeepFace](https://github.com/RiweiChen/DeepFace). To make things fun, I will add the option to add your own face to the database so you can be identified by Kat.

One other option would be to use [HyperFace](https://arxiv.org/pdf/1603.01249.pdf) for real time detection, but I will see which system is more computationally efficient.

### Emotion

* __Facial emotions__
We will use a Deep Neural Network model made in Tensorflow. The training will be done using the [Radboud Faces Database](http://www.socsci.ru.nl:8180/RaFD2/RaFD?p=main) or [Paul Ekman's database](https://www.paulekman.com/).

* __Sentiment Analysis__
A [research paper](http://www.aclweb.org/anthology/D16-1024) from Peking University presented a way to do this using a Long Short Term Memory network. For this to work, I will use an [Amazon reviews database](https://snap.stanford.edu/data/web-Amazon.html) that has 35 million samples.I will try to keep an eye out for ways to make this more efficient.

## [Bucketlist](https://github.com/takusui/Kat.ai/wiki/Bucketlist)
 
## Author notes

This will be a long journey. I created this repository with the intention to keep track of my work and hopefully become more motivated with this project. I don't know how much I can do in the following months because I have some exams to take care of, but I believe that I will start working consistently on this project after graduating this year from highschool. I'm open to new ideas and hopefully, with the experience I will gather in the next few years and with the development of open source technologies that I could use, I can bring Kat to a build that is working decently.

My main focus for now is to finish the Android app and move on to the cross-platform one. When I think about what this would look like in its final version, I imagine something like a next-gen Alexa that you can interact with fully. More than that, I want to enable her to learn on her own, like a child that you teach for a while to ride a bike and then take off its training wheels. Let us hope that the singularity will never happen.

More info can be found on the wiki.
