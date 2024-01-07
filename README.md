
# Agent Coulson: Your AI Assistant for Sustainable Startups

## Introduction:
Developing as an innovative AI helper, Agent Coulson aims to significantly change the evaluation environment for businesses in the circular economy. Beyond traditional evaluations, it performs a thorough study that includes competitor research, problem and solution exploration, risk severity assessment, market sustainability examination, investability definition, and thorough solution descriptions. Decision-makers in the startup ecosystem will find the tool invaluable as it offers practical recommendations for potential optimisations, which is its unique feature.

## Alignment with Evaluation Concepts:
- Idea Validator: Agent Coulson aligns closely with the Idea Validator concept. It focuses on developing precise explanations, rational metrics, and evaluates viability, scalability, investability, along with suggesting potential optimizations and assessing competition.

- Moonshot Finder: Agent Coulson does not align with the Moonshot Finder concept, as it doesn't specifically target revolutionary or groundbreaking concepts. However, it evaluates the potential for innovation within proposed ideas.

- Idea Filter: Agent Coulson aligns with the Idea Filter concept. It filters out unsustainable or irrelevant ideas, ensuring that only relevant and workable concepts are taken into account. Additionally, it checks for spam to maintain the quality of ideas.

## Innovative Idea:
The innovative basis of Agent Coulson is its prompt-driven approach. The algorithmic tool simplifies decision-making processes by quickly suggesting actionable insights when users enter problems and proposed solutions. Agent Coulson serves as a proactive helper, increasing user engagement and assisting in more knowledgeable and effective startup evaluations by providing details about solutions, scalability, investibility, the severity of risk, competition, sustainability.

## Technical Implementation: 
We began the training process by using API communication and tapping into the extensive dataset provided by the Digital Data and Design (D^3) Institute at Harvard. This dataset consisted of problem-solution pairs obtained from a global crowdsourcing contest focused on promoting circular economy solutions. The contest sought innovative ideas from diverse industries, including textiles and food waste management.

Our development approach incorporated generative AI tool such as GPT-3.5 turbo. The utilization of these tools allowed our model to understand and generate human-like text, enabling it to comprehensively evaluate circular economy business ideas.

```ruby
problem_statement=df.problem[1]
proposed_solution=df.solution[1]
response = client.chat.completions.create(
  model="gpt-3.5-turbo-1106",
  response_format={ "type": "json_object" },
  messages=[
    {"role": "system", "content": "You are a helpful assistant designed to output JSON."},
    {"role": "user", "content": f"{problem_statement}\n\nSolution: {proposed_solution} \nYou are a Agent who is designed to provide effective short summary of every idea presented to you fill in each and every parameter differently and  effectivey. The paramters are 1.SolutionDescription:a one or two word to describe the solutions, 2.Risk:calculate the risk in terms of high low or medium and tell the reason, 3.Competition:is there any other company or organization with same principles,4.Investable:should we invest in it or not,5.Potential_Optimisations:potential optimisation, 6.Spams: A yes or no which tells if it is idea or just a spam 7.Sustainable:also judge the idea if it is sustainable or not according to if it falls under the circular economy, considers these questions as parameteres, DO NOT CHANGE THE PARAMETER NAME OR NUMBER OF PARAMETERS"}
  ]
)
```
## Solution Description:   
Definition: A concise one or two-word description that captures the essence of the proposed solution or startup idea.  
  Purpose: To provide a quick and focused overview, allowing users to grasp the nature of the solution at a glance.

## Risk:   
Definition: An assessment of the level of risk associated with the startup idea, categorized as high, medium, or low.  
  Purpose: To inform investors about potential challenges or uncertainties related to the idea, aiding in risk management and decision-making.      
  High:  Significant regulatory, environmental, or market challenges pose substantial risks to the success of the solution  
  Medium: There are identifiable risks, but they are manageable with careful planning and execution.    
  Low: Minimal risks or robust strategies are in place to mitigate potential challenges effectively.

### Competition:    
Definition: Identification of other companies or organizations that operate with similar principles or offer comparable solutions.    
  Purpose: To understand the competitive landscape and potential market saturation, helping investors gauge uniqueness and market positioning.  
  High: Numerous competitors with similar principles exist, indicating a crowded market.    
  Medium: Some competition is present, but the solution maintains differentiating factors.  
  Low: Limited or no direct competitors with comparable principles, suggesting a potentially unique offering.

### Investable:     
Definition: A recommendation on whether investors should consider investing in the startup idea or not.   
  Purpose: To guide investors in making informed decisions based on the overall evaluation of the idea's potential for success.

### Potential Optimizations:    
Definition: Suggestions for potential improvements or optimizations that could enhance the viability or efficiency of the startup idea.   
  Purpose: To provide constructive feedback to entrepreneurs and investors, encouraging continuous improvement and innovation.

### Spam:   
Definition: A binary classification (yes or no) indicating whether the idea is a genuine, viable concept or if it might be considered spam or irrelevant.     
  Purpose: To filter out non-serious or non-sustainable ideas, ensuring a focused evaluation process.

### Sustainable:    
Definition: Assessment of whether the startup idea aligns with principles of sustainability, particularly within the context of the circular economy.   
Purpose: To evaluate the long-term environmental, social, and economic impact of the idea, supporting sustainable development goals.
These parameters collectively provide a holistic evaluation framework, addressing key aspects ranging from the nature of the solution to its potential impact and alignment with sustainability principles.



## Innovative Uses and Unexpected Outcomes
The AI assistant showcased unexpected creativity in generating optimization recommendations. It demonstrated the ability to propose unconventional strategies and alternative technologies for sustainable startups, contributing innovative perspectives to the decision-making process.

## Other Technological Tools

- Platform and Version Control:Google Colab
- Programming Language:Python 

## Future Prospects
### Advanced Model Integration:
Explore the integration of more advanced language models beyond GPT-3.5 Turbo as they become available. Stay abreast of research breakthroughs and continually upgrade the underlying AI architecture for enhanced natural language understanding.  

### User Customization Features:
Develop a user customization module allowing investors to tailor the AI assistant's analysis based on specific criteria, preferences, and industry focus. This customization will enhance the tool's adaptability to diverse investment strategies.     

### Extended Parameter Analysis:
Expand the parameterized analysis to include additional dimensions, such as social impact, scalability, and market trends. User feedback will be crucial in identifying relevant parameters for a more comprehensive startup evaluation.    

### Collaborative Decision Support:
Implement features supporting collaborative decision-making among investment teams. Real-time collaboration tools, discussion forums, and shared dashboards will facilitate efficient group evaluations of sustainable startup ideas.   

### Integration with External APIs:
Explore partnerships and integrations with external data providers, such as environmental impact databases, market trend analytics, and regulatory compliance sources. This will enhance the AI assistant's contextual awareness and improve the accuracy of its predictions.

The integration of speech-to-text (STT) and text-to-speech (TTS) functionalities is a significant step forward in achieving a more versatile and user-friendly experience.

## Limitations

Due to lack of resources as our OpenAI account was free and trail based we were bound by 3 request per minute.

