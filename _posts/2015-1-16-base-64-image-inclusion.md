Hey all;

I was recently making a mobile application in which there was a requirement to
display the image dynamically per user;

I had a constraint with me: All my data has to be in the form of WEB-SERVICE
that too Jax-WS Specification and SOAP based. I got hands on with the ADF but
didn't know that it could render the data as it is in HTML5.;

Seriously its a big W-O-W.;

So here the technique goes like this. We have some random image on the server
and its stored in the Database, Now you have the image stored as a blob Object.;

This method is going to be useful when Orgs providing the image in their API.;

Convert the Image to BASE 64 and store that into a variable make sure your image
is not very large on the server side otherwise it is going to consume a lot of
Data.;

Make everything optimal, exactly the size what you need, Scale it on the server
side if possible.

Return the String through the Application Service.;

Server Side coding
`
public Image getFlower(String name) throws IOException {

     byte[] bytes = getFlowerBytes("rose");
          return getImage(bytes, false);
	  }
	  `

	  The Image Method:

	  `
	  private Image getImage(byte[] bytes, boolean isThumbnail) throws
	  IOException {
	      ByteArrayInputStream bis = new ByteArrayInputStream(bytes);
	          Iterator readers =
		  ImageIO.getImageReadersByFormatName("jpeg");
		      ImageReader reader = (ImageReader) readers.next();
		          Object source = bis; // File or InputStream
			      ImageInputStream iis =
			      ImageIO.createImageInputStream(source);
			          reader.setInput(iis, true);
				      ImageReadParam param =
				      reader.getDefaultReadParam();
				          if (isThumbnail) {
					          param.setSourceSubsampling(4,
						  4, 0, 0);
						      }
						          return reader.read(0,
							  param);
							  }
							  `
							  Put the response in
							  your html component. 
							  and you are done. 
							  You can test the
							  response by directly
							  pasting the Byte Array
		  to the img-src as show
  in the tag.
							  `
							  ![](data:image/jpeg;base64,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)

							  `
