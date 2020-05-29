### CHATBOT using Javascript:

Live Application Demo:

https://sandysanthosh.github.io/Chatbot-JAVA/


![image](https://user-images.githubusercontent.com/11579239/83252191-706dda00-a1c8-11ea-8d05-78c301a971c7.png)



### CHATBOT using Java:

https://github.com/sandysanthosh/Chatbot

https://howtodoinjava.com/ai/java-aiml-chatbot-example/

## AIML: 
         ARITIFICAL INTELLIGENCE MACHINE LANGUAGE
         xml based markup language human interface
          aliebot what is chat-bot

A.L.I.C.E

            simple to program
            easy to understand
            highly maintable
      
### Create a Folder LIB

          add AB.jar
          
### create a folder Src/main/  -> resources -> add Bots Folder
          

#### Alicebot:

      ab.util
      ab.*;

artifical linguistic internet company entity

open source project:

### first step:

  Ab.jar

## maven pom.xml:

                <dependencies>
                    <dependency>
                      <groupId>com.google</groupId>
                      <artifactId>Ab</artifactId>
                      <version>0.0.4.3</version>
                      <scope>system</scope>
                      <systemPath>
                      ${basedir}/lib/Ab.jar
                      </systemPath>
                    </dependency>
                  </dependencies>

 ## AIML FILE:
 
 
            <aiml version ="2.0">
            <category>
            <pattern>what is you name</pattern>
            <template>ar</template>
            </category>
            </aiml>
            
## Chat.java:

                  package chatbott;
                  import java.io.File;
                  import org.alicebot.ab.*;
                  import org.alicebot.ab.utils.*;
                  public class chat {


                    private static final boolean TRACE_MODE=false;

                    public static void main(String args[])
                    {
                      try {
                        String resourcepath=getpath();
                        MagicBooleans.trace_mode=TRACE_MODE;
                        Bot b=new Bot("super",resourcepath);
                        Chat chatsession=new Chat(b);
                        String textline="";


                        while(true)
                        {
                          System.out.println("YOU : ");
                          textline=IOUtils.readInputTextLine();

                          if(textline==null || textline.length()<1)
                          {
                            textline=MagicStrings.null_input;

                          }
                          else if(textline.equals("q"))
                          {
                            System.exit(0);
                          }
                          else if(textline.equals("wq"))
                          {
                            b.writeQuit();
                            System.exit(0);
                          }
                          else
                          {
                            String request=textline;
                            String response=chatsession.multisentenceRespond(request);
                            System.out.println("BOT :"+response);
                          }

                        }
                      }
                      catch (Exception e){

                      }
                    }
                    private static String getpath()
                    {
                      File currd=new File(".");
                      String path=currd.getAbsolutePath();
                      String resourcepath=path + File.separator +"src" + File.separator +"main" +File.separator +"resources";
                      return resourcepath;
                    }
                  }


### Run a Program:

       run -> chat.java ->check in console
