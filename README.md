# speech-to-text

# first install PyAudio module
pip install PyAudio
# install speech recognition package
pip install speechRecognition

# code
import speech_recognition as sr

r= sr.Recognizer()

with sr.Microphone () as source:
	print('speak anything')
	audio=r.listen(source)
	
	try:
		text=r.recognize_google(audio)
		print ('you said :{}'.format(text))
	except:
		print ('sorry not clear audio')
	

