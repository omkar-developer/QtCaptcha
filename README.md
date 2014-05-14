QtCaptcha 1.0
=========

Captcha generator for Qt

Usage Example : 

  	QPainter painter(this);
	Captcha cp;
	cp.generateText();
	painter.drawImage(30, 30, cp.captchaImage());
	
	
Example 2 : 

  	QPainter painter(this);
	Captcha cp;
	cp.randomize();
  	cp.setDifficulty(3);
	cp.generateText();
	painter.drawImage(30, 30, cp.captchaImage());

Example 3 (using predefined words dictionary) : 

	QPainter painter(this);
	Captcha cp;
	cp.randomize();
  	cp.setDifficulty(3);
	cp.loadDictionary("dictionary.txt");
	cp.setTextGeneration(Captcha::TextGeneration_Dictionary);
	cp.generateText();
	painter.drawImage(30, 30, cp.captchaImage());

Difficulty Levels Screen shot: 

![Alt text](/difficultylevels.jpg?raw=true "Difficulty Levels")

Performance (intel Core i7 2630QM 2.0GHz / Single Thread):

- Difficulty 0 : 1068/s
- Difficulty 1 : 975/s
- Difficulty 2 : 843/s
- Difficulty 3 : 560/s
- Difficulty 4 : 534/s
- Difficulty 5 : 412/s


