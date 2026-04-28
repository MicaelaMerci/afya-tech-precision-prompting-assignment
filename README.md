# afya-tech-precision-prompting-assignment

##  Introduction

Precision in maternal health AI is critical because generic advice can be unsafe in rural contexts. In Kenya and Uganda, over 70% of expectant mothers live more than 5km from health facilities and rely on local foods like ugali and matooke. Context-aware prompts ensure culturally relevant, safe, and actionable guidance.


## Prompt A: Nutrition Advice

###  AIM Framework
- A (Audience): Pregnant women in rural Kenya and Uganda using SMS  
- I (Intent): Provide practical, culturally relevant nutrition advice  
- M (Mode):  Short, simple, SMS-friendly messages  

###  MAP Framework
- M (Material):  
  Local foods such as ugali, sukuma wiki, beans, matooke, and groundnuts; low-income constraints; seasonal food availability  
- A (Action): 
  Generate 3–5 daily nutrition tips using locally available foods  
- P (Persona):
  Community health worker  

### Final Prompt
Act as a community health worker in rural Kenya and Uganda. Provide 3–5 simple nutrition tips for pregnant women using locally available foods such as ugali, sukuma wiki, beans, matooke, and groundnuts. Consider low-income households and seasonal food access. Keep advice short, clear, and suitable for SMS.

###  Key Improvement
Grounds advice in local food systems, reducing irrelevant recommendations and improving usability.


## Prompt B: Appointment Reminders

###  AIM Framework
- A (Audience): Pregnant women in rural areas, often living >5km from clinics  
- I (Intent): Remind and help plan clinic visits effectively  
- M (Mode): Clear, supportive SMS reminders  

### MAP Framework
- M (Material): 
  Long travel distances, limited transport, clinic schedules, community health worker availability, and financial constraints (e.g., reliance on mobile money such as M-Pesa)  
- A (Action):
  Generate reminders including appointment date, travel planning, and support options  
- P (Persona):
  Maternal health assistant  

###  Final Prompt
Act as a maternal health assistant sending SMS reminders to pregnant women in rural Kenya and Uganda. Remind them of upcoming clinic visits, considering that many live more than 5km away and need to plan transport and costs. Include the clinic date, suggested travel time, and availability of community health workers if applicable. Keep the message short, supportive, and clear.

###  Key Improvement
Incorporates real-world constraints (distance, cost, transport), making reminders actionable instead of generic.


## Prompt C: Emergency Triage

###  AIM Framework
- A (Audience): Pregnant women experiencing symptoms in rural settings  
- I (Intent): Provide safe, step-by-step triage guidance  
- M (Mode): Calm, clear, non-panic SMS guidance  

### MAP Framework
- M (Material): 
  Limited access to hospitals, reliance on community health workers, and common danger signs (e.g., bleeding, severe headache, reduced fetal movement)  
- A (Action): 
  Assess symptoms and guide next steps  
- P (Persona):
  Trained maternal health triage assistant  

###Final Prompt (Chain-of-Thought + Verifier)
Act as a trained maternal health triage assistant for rural Kenya and Uganda.

Step 1: Ask the user to clearly describe their symptoms.  
Step 2: Classify symptoms as mild, moderate, or emergency (e.g., severe bleeding, severe headache, no fetal movement).  
Step 3: Provide guidance:  
- Mild → home care and monitoring  
- Moderate → contact a community health worker  
- Emergency → go to the nearest clinic or hospital immediately  

Step 4: Use a calm and reassuring tone.

Verifier Step: 
- Ensure enough information is collected before advice  
- Do not delay urgent care  
- Avoid harmful or incorrect guidance  
- Clearly prioritize emergency symptoms  

###Key Improvement
Introduces structured reasoning and safety verification, reducing risk of harmful or panic-inducing advice.


##Reflection

This assignment highlights the importance of designing AI systems that are context-aware and user-centered. Applying AIM and MAP frameworks improves relevance by incorporating local realities such as food availability, distance to healthcare, and financial constraints. The use of structured reasoning and verification enhances safety, ensuring that advice is reliable and appropriate. Overall, effective prompt design is essential for building responsible AI solutions in healthcare, especially in underserved communities.





#  Savannah Adventure: Precision Prompting Challenge

##  Introduction

This assignment explores how AI prompts can fail when they ignore real-world constraints in rural healthcare contexts. In Kenya and Uganda, maternal health advice must consider local food systems, access to clinics, transport limitations, and cultural realities. This exercise applies AIM, MAP, Verifier, Chain-of-Thought, and OCEAN frameworks to improve AI reliability and safety.



##  1. MAP Framework Failure (Nutrition Advice)

###  Problem
AfyaTech’s AI advised: *“Eat more leafy greens like kale.”*

This failed because kale is not commonly available in Kakamega County, making the advice impractical.



###  Why the Failure Happened (MAP Analysis)

- M (Material):
  The prompt ignored local food availability and assumed global dietary access.

- A (Action): 
  The instruction was too generic (“give nutrition advice”) without local adaptation.

- P (Persona): 
  No local health worker context was defined, so the AI defaulted to global advice.



### Improved Prompt (Local Food System Anchored)

Act as a community health worker in Kakamega County, Kenya. Provide simple nutrition advice for pregnant women using locally available foods such as sukuma wiki, kunde, beans, ugali, and groundnuts. Ensure advice is affordable, culturally appropriate, and based on seasonal availability.



###  Key Improvement
The prompt now uses locally available foods, making advice realistic and usable in rural settings.



##  2. Verifier Pattern (Emergency Triage)

###  Problem
Original prompt: *“Visit your doctor immediately if you have abdominal pain.”*

This caused panic and ignored financial and transport barriers.



### Improved Prompt Using Verifier Pattern

Before giving advice, the AI must ask:

- How severe is the pain?  
- How long has it lasted?  
- Any other symptoms (bleeding, fever, dizziness)?  
- How far is the nearest clinic or health worker?  


###  Response Logic

- Mild: Rest and monitoring  
- Moderate: Contact community health worker  
- Severe: Immediate medical attention  


###  Verifier Check

Before responding, ensure:
- Enough context is collected  
- No unnecessary panic is caused  
- Access barriers are considered  
- Emergency cases are prioritized  


###  Key Improvement
Prevents panic by ensuring the AI asks questions first before giving medical advice.


##  3. Chain-of-Thought vs WHO Summarization

Competitors use verbatim summaries of WHO guidelines from the World Health Organization.

However, Chain-of-Thought reasoning creates more value because it:

- Breaks down global guidelines into simple steps  
- Adapts advice to rural realities (distance, cost, CHWs)  
- Translates medical language into SMS-friendly instructions  
- Prioritizes actionable decisions over theory  

For example, instead of saying “attend antenatal visits regularly,” the AI reasons that many women live far from clinics and suggests integrating community health worker support.


### Key Insight
Chain-of-Thought transforms AI from a passive summarizer into an adaptive decision-support system tailored for rural East Africa.


##  4. OCEAN Framework (Data Accuracy Check)

### Problem
Report stated: *“Kenya has 1.8 doctors per 10,000 people.”*  
This is outdated (2025 actual: 0.9 per 10,000).


### How OCEAN Detects This Error

- O (Observe): Identify statistical claims in reports  
- C (Check): Verify against updated sources (government/WHO databases)  
- E (Evaluate): Assess accuracy and relevance for 2025  
- A (Act): Replace or correct outdated figures  
- N (Note): Document source and uncertainty  



### Key Improvement
Ensures data accuracy and credibility before sharing information with donors or stakeholders.


## Conclusion

This exercise demonstrates that effective AI in healthcare must go beyond generic responses. Using structured frameworks like AIM, MAP, Verifier Pattern, Chain-of-Thought, and OCEAN ensures that AI systems are safe, context-aware, and relevant to rural populations. Proper prompt design reduces harm and improves real-world usability in maternal health systems.
