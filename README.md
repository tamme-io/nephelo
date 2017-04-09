# nephelo
A Cloud Formation library to more easily create AWS Infrastructure programatically. Nephelo, short for Nephelococcygia, is the art of watching clouds.

This is under construction, and though it has successfully deployed a multi region application, it is some of the worst code written.
There is no documentation, there is no error handling, there are no warranties, guarantees or even tests.

In fact, it would seem unwise to use this library at all in it's current form.

#### WARNING ####

This library is under construction, under no circumstances should you use it in a production environment.


##### USAGE #####
###### Don't - read warning above ######

CLI - nephelo {command} [arguments]

 - nephelo get {module} {stage}
   - nephelo get network development
   - nephelo get compute development

 - nephelo save {stage}

 - nephelo delete {stage}
 
 - nephelo deploy {stage}
 
 
Templates

${variable} - this will be replaced with anything in the nephelo.json file

@{reference} - this will create a reference to another object

!{subnets} - will provide a reference to each of the subnets in a network

!{subnets[0]} - will get a reference to the first subnet

@@{ENV_VARIABLE}@@ - this will try to find an environment variable and replace, otherwise it will replace with an empty string

%{ raw-subnet-ids as |subnet|, 
		{TEMPLATE}
	}% - will iterate over the subnet ids and create a thing, this should be able to be used with any array in the nephelo.json file
	
	
#
File Structure

notes to come