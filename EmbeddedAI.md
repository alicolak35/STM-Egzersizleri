## Philosophy of the exercise 

The following is a set of high-level questions on real-time DNN-based processing and network deployment on the edge. 
There is no gold answer and hopefully no ready-to-copy answers on the web as well. 
The goal is not to spend too much time on it, but to gather your knowledge and thoughts before discussing.

You can submit your answers in any written way you'd like (e-mail, Word document, .md, Github Repo, etc..), as long as the questions are answered. 

Good luck, and have fun ! 🙃


## Interview questions

1. Could you describe the advantages and disadvantages of using a framework such as PyTorch or Tensorflow in implementing a DNN in an embedded context versus using specific solutions such as Tensorflow Lite or a specific ONNX-based runtime?

---

2. Imagine you have selected a particular model and can no longer change its design. What are the key parameters to be taken into account in the model when selecting an MCU that will be used to implement this DNN? How can you measure it ? 

---

3. Can you describe a few strategies related to model optimization in the context of edge deployment?

---

4. When training a DNN with recurrent layers in a real-time audio context in frameworks such as PyTorch or Tensorflow, the network input (of shape [batch_size, audio_channels, L, N]) contains all L audio blocks of N samples. We do this to speed up the training process (we call this offline implementation). In the offline implementation, the state of the recurrent layers is managed internally by the frameworks (each recurrent layer will return a sequence of L blocks of output and a state always of length L blocks). How would you handle the problem of state management in the recurrent layers in the case of an online implementation (in the case in which the network receives blocks of N samples sequentially)?

---

5. In real-time audio processing, an input audio stream is processed by the DNN in blocks of N samples. You can imagine each block as a 1D signal input to the DNN, the network receives these inputs sequentially. What would be your strategy to develop a convolutional model capable of identifying temporal patterns longer than N samples? What should you take into account in the embedded implementation of your solution?

---

6. Which are the main advantages of employing a real-time scheduler? Can you briefly describe a few real-time scheduling algorithms highlighting these advantages?

---

7. Have you ever write code without an OS (bare metal)? If so, could you describe the steps needed from writing your code to executing to a specific platform of your choice? Can you highlight the advantages of employing an OS?

---

8. Explain fixed-point math. How do you convert a number into a fixed-point, and back again? Have you ever written any C functions or algorithms that used fixed-point math? Why did you?

--- 

9. Pulse Audition develops hearing glasses to help people suffering from hearing loss better understand speech in noisy environments : The Pulse Frames. 
They are composed of 

- 5 microphones 
- A Bluetooth chip for classical signal processing and audio streaming
- An AI accelerator
- A stereo amplifier
- Two speakers

The microphone signals are processed by a mix of signal processing and deep learning on both chip before being sent to the speakers (from the Bluetooth chipset). 
The physical comes with an app to control settings, take calls and listen to music. 

Please draw a functional diagram of the architecture including as much detail as possible (communication protocols, frequencies, latency, etc.)


### Subsidiary questions
1. When should your internship ideally start and finish ? 
2. Are you comfortable relocating to Cote d'Azur for the internship ? 
3. What are you wage expectations ? 
3. Will you need a visa to come work in France ? 
