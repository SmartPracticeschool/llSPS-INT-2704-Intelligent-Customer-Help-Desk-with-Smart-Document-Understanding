# llSPS-INT-2704-Intelligent-Customer-Help-Desk-with-Smart-Document-Understanding
## Intelligent Customer Help Desk with Smart Document Understanding

The typical customer care chatbot can answer simple questions, such as store locations and hours, directions, and maybe even making appointments. When a question falls outside of the scope of the pre-determined question set, the option is typically to tell the customer the question isn’t valid or offer to speak to a real person.

In this project, there will be another option. If the customer question is about the operation of a device, the application shall pass the question onto Watson Discovery Service, which has been pre-loaded with the device’s owners manual. So now, instead of “Would you like to speak to a customer representative?” we can return relevant sections of the owners manual to help solve our customers’ problems.

To take it a step further, the project shall use the Smart Document Understanding feature of Watson Discovery to train it on what text in the owners manual is important and what is not. This will improve the answers returned from the queries.

## Project Scope

  *Project Requirements:*

   * IBM Cloud
   * IBM Watson services
   * Node Red
   * Web Framework

*Functional Requirements:*

   * A Chatbot able to answer queries.
   * Redirect the operational queries to Owner's manual.
   * Redirect the query to the particular section of the owner's manual.


*Technical Requirements:*

   * Create a chatbot using Watson Assistant.
   * Use Watson Discovery to  redirect the user's query to the section of the owner's manual.
   * Use Node Red to wire together Api and online services.
   * Integrating it with IBM Cloud.

*Software Requirements:*

   * IBM watson services
   * IBM Assistant
   * IBM cloud
   * Github
   * Node red
   * User interface
   * Security
   * Json editor


*Project Deliverables:*

   The model created i.e. a chatbot would be able to identify any operational question posted by the user
   and using IBM Watson discovery will redirect the user to the  section of the owner's manual
   where the answer to the question lies.
    
 
 ## Flow
 ![Image description](https://github.com/IBM/watson-discovery-sdu-with-assistant/blob/master/doc/source/images/architecture.png)
 
 This flow basically summarizes the project. It begins with :
 
1. The annotation of document using Watson Dicovery SDU.
2. The user interacts with Node-Red app UI.The chatbot engages the user in conversation.
3. Dialog in this interaction is coordinated by Watson Assistant.
4. If the customer asks a technical question, it will be passed to Cloud Functions action.
5.This action will further pass onto to Watson Discovery and return with appropriate solution.

