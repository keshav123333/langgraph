# langgraph




traditional ai-> ye input and target ke bich ka difference dhundne ki kosi karta hai whereas 

gen ai-> data ka distribution samjhne ki kosis karta hai instead of ki like input out so isse vo samjhta hai 


agentic ai -> ye kuch goal acheive karke deta hai steps m gen ai isme reactive isme apko khud batana padta ki ab kya karna hai ab kya kar whereas 
agentic ai gen ai ko use karta hai apne goal ko achive karne mein



lecture 3 

agentic ai have some property 

autonomy -> means excution decsion making karna padta hai and reasoning and adaptive hona chaiye like bich mein kuch cheez ya eeror 
eg maan mujhe full stack dev chaiye the but achank se mujhe freelancer hire kar raha so iss agent ko dekhna padega ki ye aise kaam kare ki changing task ko handle 


brain-> llm, tools-> api  and ek supervisor-> jo ki human ya vo agent bhi ho sakta



lecture 4 -> dekh workflow kaise bana raha hai vo important hai
understand workflow kaise banta hai and batya hai langchain and langgraph kyon use karte 


langchain disadv -> story se samjh 
 maan le ek workflow jisme hume continouly ek company ko mail dena jab tak return main mail na aa jaye for approval of our position in that company
 so iske liye loop lagega and loop ho gaya ye langchain m banae ke liye while loop alag se likhna padega isme bahar se code use tera 
 2 cheez maan le chal ab ye bhi ho gaya ab tera maan kiya ki mujhe abhi ek code likna jisme jump ho ki if ye ni toh teen chaar cheezon ko jump karke aage badh ja and 
maan le condition loop lagan bhi mushkil hota 

yaha langgraph
glue code -> matlab ki agar mujhe kuch aise cheezein karni hai jo langchain m nahi hai toh uske liye code likhna padta hai aur usko langchain se connect karna padta hai python ka code likhna pada while loop ke liye so ye glue code hua 


langchain m memory hoti hai par vo converational memory hai and state handling ni hoti iska video

WATHC VIDEO DEKH LE LIKE LANGCHAIN VS LANGGRAPH WALA LECTURE 4 



langgrpah mein like ek dict banti hai uss dict mein like state ko store jaise maine ek fireld kya weather then kya humne abhi tak kitni website dekhi and bahut sari cheezon ki dict bana  leta ye 
and har node isme cheeze change and add kart rehta so like samjh raha hai sab milke kuch kaam kar rahe hai 


event driven arch hai langgrpah ->
like isme exampl le do chain pehli chain email send to candidate and dusri chain 7 din wait karegi and jab reply aaye tab hi vo chain excute 
so ye kaam langchain mein ni ho sakta 


langgraph long running workflow banane ke liye bhi acha as 7 din wait kar then vo chala 

langgraph fault tolerance hai as like maan kuch stage pe server down so langchain usse checkpoit save toh vaha tak ka sab kuch save and jab server up toh vahi se restart 



lecture 5 dekh usem alag alg type ke workfollow ke liye tecnique batayihai like parallel ya aggregator workflow ko dekh video 

# Graph

langchain mein workflow if tu grpah ki form m bana skata toh vo langchain m bhi ban sakta example maan le ek task 
1. write an essay hum uss essay ko multiple cheezo pe evaluate and then output denge if esssay acha toh thik varna usskosudharne ka suggestion denge

<img width="836" height="616" alt="Screenshot 2026-03-28 125223" src="https://github.com/user-attachments/assets/054ea9a5-6310-4a5f-8876-f6898b6854f9" />



## states

ye ek type ki dict hoti jo genrally typed dict hoti pydantic bhi use kar rskate ho
ye har waqt apke har node ke pas available so if koi change karna toh vo isme kar sakta hai and apne hisab se usko like change ya info gatehr kar sakta hai 


iska pic example 
<img width="854" height="473" alt="image" src="https://github.com/user-attachments/assets/56339635-1adb-4e33-8957-357022e1773e" />



# reducer 

maan le ek case hai chatbot and state hai dict jisme msg so ek chat hui usme hii my name is keshav save then dusri baar main puch capital of delhi so vo pehle wale chat ko dict state m se hata ke lsg m ab ye save so ye toh galat as mujhe toh sab kuch bhejna tha so msg mein hum ek add name se cheez aaddd so ab yaha pe chat add hoti rahenge isntead of removing 


and like reducer ki help se set ki ek key dict ki koi value store ya maan nayi value aaye toh vo purani m add ho jayeg ya merge ya replace purani wali se nayi wali value 

