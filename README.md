# News Article Scraper 

Many of the APIs that I came across provided only the headlines and urls of the news articles. None of them provided the content of that news article. The content of news may be required to apply various Machine Learning and Natural Language Processing techniques to improve the functionality of news websites. 

Thus in this project I have used the newsapi provided by [newsapi.org](newsapi.org)
The json data provided by this api is in the following manner

```python
{
	'articles': [
			{
				'author': 'Fleet Street Fox',
				'description': 'The alternative coalition of lexical chaos would see us all tweeting about Ed Balls',
				'publishedAt': '2017-04-28T12:35:03Z',
				'title': 'A strong, stable leader needs strength, stability and a stable, strong message',
				'url': 'http://www.mirror.co.uk/news/uk-news/strong-stable-leadership-needs-3-10314956',
				'urlToImage': 'http://i4.mirror.co.uk/incoming/article10314310.ece/ALTERNATES/s1200/fleet-may.jpg'
			},
		       {
				'author': 'Voice of the Mirror',
				'description': "The Tories' cruel \xa33bn cuts plan has left the education system teetering on the brink of collapse, according to unions",
				'publishedAt': '2017-04-27T21:40:43Z',
				'title': "Voice of the Mirror: May's grim propaganda exposed by destruction of schools",
				'url': 'http://www.mirror.co.uk/news/politics/voice-mirror-theresa-mays-grim-10311950',
				'urlToImage': 'http://i3.mirror.co.uk/incoming/article10311108.ece/ALTERNATES/s1200/PROD-Britains-Prime-Minister-Theresa-May-ges.jpg'
			},
			.
			.
			.
		   ]
}
```

When you run the file 'fetchApiData.py', a new dictionary has been created with the key "data" which contains the content of the article from the url provided by "newsapi".

Output :
```python
{
	'articles': {
			'article_0': {'data': "Thank you for that totally unstaged round of applause to this snap general election column which is the only one you will find that can provide the strength and stability to enable Britain to safely chart the uncertain waters of praying for the sweet release of death. That strength and stability doesn't sort itself out: the person in charge of this column must provide the steady hand on the linguistic tiller in a manner which is not just strong, but also stable, in order to avoid the rocky shoals which will melt extended metaphors to shreds.  The alternative to this powerful strength and unwavering stability would be the sort of lexical chaos which has led THE LABOUR PARTY to tweet the words 'Ed Balls' on an annual basis for over six years now, despite a total lack of evidence that it provides any solidity or oomph to things.  It is only strength, and stability, that can save us from that kind of pandemonium which will, ultimately and without steadfast and stout stewardship, send our nation chicaning wildly through synonyms like Jeremiah Clarke's son on Top Ganja. And it is that vigour, that toughness needed to keep us all on an ideological path three quarters of this nation didn't vote for, which only I can provide through the support and security you all feel from the devil you think you know.Frankly, my record of being stable and strong speaks for itself. Under my leadership I have shown our education system the strength to reformulate the school funding formula to give all headteachers the stability of knowing they'll have to confiscate \xa33billion from unruly, and frankly weak and unstable, pupils if they want to provide them with the books they need to learn how trustworthy and powerful I am.  As leader I am leading us not into a General Election but a leadership campaign in which we'll keep mentioning my strong, stable and leaderly-sounding name THERESA MAY and the other chap's chaotic and conspiratorial-sounding name JACOBIN TRAITORYN because that's what a solid and dependable leader does if the name of their party is toxic to the 48% who didn't want to Leave, the 9m who voted for Ed Manbag and most of our own members who think Brexit means something else.  Being a leader means leading in a manner which is both stable and, as I've been very clear, strong. That's why under my leadership you don't need to worry about a fall in house prices or a slump in GDP, because sound and steadfast leadership will soon lead us to the sunny, sunlit, upland foothills of going forward to the place we used to be that is better than it was. That's the kind of vision which being a strong and stable leader is all about. I am going to be out here, every day, leading from the front, whenever I am not leading in Westminster which of course is when leading Britain on the world stage isn't taking up all of my time, talking to people all over the country from all walks of life so long as they are Theresa activists, #dontmentiontheTories.  What I won't be doing, and I can absolutely promise you this, is the kind of weak and destabilising activities undertaken by JERRY OFF THE GOOD LIFE like chaotically taxing people more, unsteadily offering not to randomly bomb whoever Mr Trumpet wants to obliterate next, doubtfully securing NHS and social care and launching an uncertain and ill-thought out campaign to take decisive action on violence against women and girls. After all, I'm a girl, and I'm a leader, so no-one else should have any problems at all. At the same time I will be resolute and determined in remaining constant in an established fashion on securing my courageous and potent leadership plan for leading us out of disunity and into being the ones in charge of leading again by focusing intently on a point upon a philosophical horizon that totally ignores my own role in increasing knife crime and the lack of any ideas to deal with rising homelessness which is the fault of the previous administration I was part of let's move on.  Strength and stability is the central and most integral part of my campaign to be leader of the UK, not the Queen I have all her power now.  It's also my favourite Jane Austen novel, along with vigour and vitality, influence and immobility and of course competence and credibility, not one of which I am sure my opponent THE LABOUR PARTY GERBIL OF DOOM has ever read.  Being strong, and also very stable, both as a vicar's daughter and leader of my Girl Guide patrol, is so much a part of my DNA that I don't even need to use the words. We can just shorten it to SS and I'm sure everyone knows what that means, except possibly Ken Livingstone who has, and I've been very clear about this, never been a member of MY nasty party.  Give me a mandate to pretend I don't u-turn, and I'll u-turn for you in a circle of words you can never escape; give me a mandate to make you look at Brexit and ignore the welfare state burning down around your ears and I'll give Boris the matches; and give me a mandate at this turning point for a vision of strong and stable leadership and I'll lead you to a sustainable, potent and permanent vision I alone can deliver of real leadership who will be a stable leader for difficult times in need of strong leaders. We need strength. We need stability. We need a thesaurus. And I can deliver a vision of leadership that you'll have to believe if I say it often enough.",
                            'image': 'http://i4.mirror.co.uk/incoming/article10314310.ece/ALTERNATES/s1200/fleet-may.jpg',
                            'title': 'A strong, stable leader needs strength, stability and a stable, strong message'},
              'article_1': {'data': "The destruction of good and excellent schools exposes the grim reality behind Theresa May and her Tory propaganda.Who would you believe? More than 500 heads who signed a protest letter... or a politician prepared to say anything to con people into voting Tory?The price of May\u2019s \xa33billion education cuts will be paid by the children of working and middle class families in thousands of state schools. Their education will be blighted and future prospects harmed by nasty Tory spending reductions.Sacking teachers and enlarging classes, with subjects such as music out of bounds for all except the kids of parents who can afford to pay, is the ugly face of Tory rule. A Tory-heavy watchdog just tore Theresa May's free schools project to bits Should May be returned to Downing Street with a thumping majority, she would be a PM immune to pressure and able to rule arrogantly.The hundreds of heads appealing for support are the voice of reason, respected independent educators with the best interests of our children at heart.Britain faces a stark choice on June 8. The Theresa May asking working people to lend her their vote is the same Theresa May preparing to undermine the education of those same working people and reduce their living standards.The gulf between what May says and does is a harsh lesson in dishonest Conservative politics.",
                            'image': 'http://i3.mirror.co.uk/incoming/article10311108.ece/ALTERNATES/s1200/PROD-Britains-Prime-Minister-Theresa-May-ges.jpg',
                            'title': "Voice of the Mirror: May's grim propaganda exposed by destruction of schools"},
              'article_2': {'data': 'If you loved it when Miriam Margolyes took over on The Graham Norton Show or The Real Marigold Hotel, BBC Four has a treat for you hidden away on Thursday nights.Miriam is starring in Bucket, a sitcom about Mim, a terminally ill seventysomething mum, who is trying to establish a connection with her jobless and single 35-year-old daughter Fran via a bucket list.The first episode a fortnight ago was basically a platform for Miriam to behave like Miriam for half an hour.It would be a shame if that opening whirlwind put people off though. Since then she has toned it down considerably \u2013 and Bucket has turned into the sweetest comedy I\u2019ve seen in years. It\u2019s also laugh-out-loud funny, with Mim usually getting all the best lines: \u201cLove doesn\u2019t last \u2013 unlike herpes.\u201dI bet if Elton John was watching from his sickbed last night he would have appreciated the timing of \u201cSing a duet with Elton John\u201d appearing on Mim\u2019s list of things to do before she dies.Of course, no sitcom could survive an entire series of Miriam swearing, farting and flashing her boobs.Fortunately Frog Stone is brilliantly understated as Fran while Stephanie Beacham is the exact opposite as Mim\u2019s smug cousin Pat.There\u2019s only one episode left in this series but I have a feeling there might be more to come. One, because Mim\u2019s list is quite long. And two, because she\u2019s such an attention-seeker she is probably lying about dying anyway.',
                            'image': 'http://i3.mirror.co.uk/incoming/article10310706.ece/ALTERNATES/s1200/Bucket.jpg',
                            'title': 'Miriam Margolyes dials down but her Bucket list has plenty of life'},
                            .
                            .
                            .
                            .
                            so on..
              }
```

This code has been written to scrape articles from the source "Mirror". Many other news sites can be scraped. In order to add scraper for many other sites, write the scraping code in the "scraping" package.
