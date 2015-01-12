The following post is something that we all should know its about HTTPS and WEB Services.

Though its basic but its really something important for the banking and web service development perspective.

Courtesy MSDN flash.

------BEGIN_POST------

Brace yourself, here there's another coming :-)

Today I had to explain to my girlfriend the difference between the  expressive power of WS-Security;as opposed to;HTTPS. She's a computer  scientist, so even if she doesn't know all the XML mumbo jumbo she  understands (maybe better than me) what encryption or signature means.  However I wanted a strong image, which could make her really understand  what things are useful for, rather than how they are implemented (that  came a bit later, she didn't escape it;:-)).

So it goes like this. Suppose you are naked, and you have to drive your motorcycle to a certain destination.
In  the (A) case you go through a transparent tunnel: your only hope of not  being arrested for obscene behaviour is that nobody is looking. That is  not exactly the most secure;strategy you can come out with...;(notice  the sweat drop from the guy forehead :-)). That is equivalent to a POST  in clear, and when I say "equivalent" I mean it.
In the (B) case, you  are in a better situation. The tunnel is opaque, so as long as you  travel into it your public record is safe. However, this is still not  the best situation. You still have to leave home and reach the tunnel  entrance, and once outside the tunnel probably you'll have to get off  and walk somewhere... and that goes for HTTPS. True, your message is  safe while it crosses the biggest chasm: but once you delivered it on  the other side you don't really know how many stages it will have to go  through before reaching the real point where the data will be processed.  And of course all those stages could use something different than HTTP:  a classical MSMQ which buffers requests which can't be served right  away, for example. What happens if somebody lurks your data while they  are in that preprocessing limbo? Hm. (read this "hm" as the one uttered  by Morpheus at the end of the sentence "do you think it's air you are  breathing?").
The;complete;solution (c) in this metaphor is painfully  trivial: get some;darn clothes on yourself, and especially the helmet  while on the motorcycle!!! So you can safely go around without having to  rely on opaqueness of the environments. The metaphor is hopefully  clear: the clothes come with you regardless of the mean or the  surrounding infrastructure, as the messsage level security does.  Furthermore, you can decide to cover one part but reveal another;(and  you can do that on personal basis: airport security can get your jacket  and shoes off, while your doctor may have a higher access level), but  remember that short sleeves shirts are bad practice even if you are  proud of your biceps :-) (better a polo, or a t-shirt).

I'm happy to say that she got the point! I have to say that the  clothes metaphor is very powerful: I was tempted to use it for  introducing the concept of policy (disco clubs won't let you in sport  shoes; you can't go to withdraw money in a bank in your underwear, while  this is perfectly acceptable look while balancing yourself on a surf;  and so on) but I thought that for one afternoon it was enough ;-)

![](http://www.maseghepensu.it/oldblogrecovery/End2EndSecurity.jpg)

;

;

-----END----

;

Hope you all enjoyed reading it.
