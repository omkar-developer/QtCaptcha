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
