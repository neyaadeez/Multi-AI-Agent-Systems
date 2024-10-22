# Multi-Agent Systems

## Overview

This repository showcases a series of projects utilizing multi-agent systems developed with the [crewAI](https://crewai.com) framework. Each project highlights unique applications of AI agents to automate processes across various domains, including customer support, sales outreach, event planning, financial analysis, and job application tailoring. 

## Table of Contents

- [Multi-Agent Customer Support Automation](#multi-agent-customer-support-automation)
- [Customer Outreach Campaign Tool](#customer-outreach-campaign-tool)
- [Automated Event Planning](#automated-event-planning-with-crewai)
- [Multi-Agent Collaboration for Financial Analysis](#multi-agent-collaboration-for-financial-analysis)
- [Multi-Agent System for Tailoring Job Applications](#multi-agent-system-for-tailoring-job-applications)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)

---

## Multi-Agent Customer Support Automation

### Overview

This project demonstrates a multi-agent system designed to automate customer support interactions using the crewAI framework. The goal is to create a cooperative environment where agents can handle customer inquiries effectively while ensuring high-quality support.

### Key Features

1. **Role Playing**: Each agent has a defined role and backstory, allowing them to simulate realistic interactions with customers.
2. **Focus**: Agents are programmed to concentrate on their roles, which enhances the quality of the support provided.
3. **Cooperation**: Agents can delegate tasks to each other, fostering collaboration to resolve customer inquiries more efficiently.
4. **Tools Integration**: The system utilizes various tools for enhanced functionality, such as scraping documentation, accessing CRM data, and checking bug reports.
5. **Guardrails**: The system maintains quality assurance by ensuring agents operate within their defined scope.
6. **Memory**: Agents can remember past interactions, allowing for more personalized support in future interactions.

---

## Customer Outreach Campaign Tool

### Overview

The **Customer Outreach Campaign Tool** leverages multi-agent systems to optimize the process of identifying high-value leads and crafting personalized outreach strategies. Built using the **CrewAI** framework, this project demonstrates the power of AI agents in enhancing sales and marketing efforts.

### Key Features

- **Versatile Agents**: Two distinct agents collaborate to streamline the outreach process:
  - **Sales Representative Agent**: Identifies potential leads by analyzing data and trends.
  - **Lead Sales Representative Agent**: Nurtures leads with tailored communication.
  
- **Custom Tools**: Utilizes both pre-built and custom tools for agent tasks, including:
  - **Sentiment Analysis Tool**: Ensures positive communication.
  - **SerperDevTool**: Searches for relevant information to enrich lead profiles.

- **Task Management**: Guides agents in conducting lead profiling and creating personalized outreach campaigns.

### Setup

#### Prerequisites

Ensure you have the following libraries installed:

```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
```

#### Running the Project

To kick off the outreach campaign, provide input parameters such as lead name, industry, key decision-maker, position, and recent milestone:

```python
inputs = {
    "lead_name": "DeepLearningAI",
    "industry": "Online Learning Platform",
    "key_decision_maker": "Andrew Ng",
    "position": "CEO",
    "milestone": "product launch"
}

result = crew.kickoff(inputs=inputs)
```

---

## Automated Event Planning with crewAI

### Overview

This project demonstrates an automated event planning system using the crewAI framework. It leverages multiple agents to handle various aspects of event organization, ensuring a seamless planning experience.

### Features

- **Venue Coordination**: Identifies and books suitable venues.
- **Logistics Management**: Manages all logistical aspects, including catering and equipment.
- **Marketing and Communications**: Promotes the event and engages with potential participants.

### Usage

1. Set up API keys and initialize the agents.
2. Provide event details to the crew and kick off the planning process.

### Example Code

```python
# Initialize the crew and run the planning system
event_management_crew = Crew(
    agents=[venue_coordinator, logistics_manager, marketing_communications_agent],
    tasks=[venue_task, logistics_task, marketing_task],
    verbose=True
)

event_details = {
    'event_topic': "Tech Innovation Conference",
    'event_description': "A gathering of tech innovators to explore future technologies.",
    'event_city': "San Francisco",
    'tentative_date': "2024-09-15",
    'expected_participants': 500,
    'budget': 20000,
    'venue_type': "Conference Hall"
}

result = event_management_crew.kickoff(inputs=event_details)
```

---

## Multi-Agent Collaboration for Financial Analysis

### Overview

This project leverages multi-agent systems to perform real-time financial analysis, focusing on stock market trading.

### Features

- **Data Analyst Agent**: Monitors and analyzes market data.
- **Trading Strategy Developer Agent**: Refines trading strategies based on data insights.
- **Trade Advisor Agent**: Suggests optimal trade execution strategies.
- **Risk Advisor Agent**: Evaluates risks associated with trading activities.

### Example Usage

```python
financial_trading_inputs = {
    'stock_selection': 'AAPL',
    'initial_capital': '100000',
    'risk_tolerance': 'Medium',
    'trading_strategy_preference': 'Day Trading',
    'news_impact_consideration': True
}

result = financial_trading_crew.kickoff(inputs=financial_trading_inputs)
```

---

## Multi-Agent System for Tailoring Job Applications

### Overview

This project demonstrates a multi-agent system to help job applicants tailor their resumes and prepare for interviews.

### Features

- **Research Agent**: Analyzes job postings for key qualifications.
- **Profiler Agent**: Compiles a comprehensive profile of the applicant.
- **Resume Strategist Agent**: Tailors resumes to highlight relevant skills.
- **Interview Preparer Agent**: Develops interview questions and talking points.

### Outputs

The system generates:

- `tailored_resume.md`: A tailored resume.
- `interview_materials.md`: Interview questions and talking points.

---

## Installation

To run the projects locally, install the required libraries:

```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
```

## Usage

Refer to the specific sections for each project to understand how to set up and run the corresponding systems.

---

## Acknowledgments

- Thanks to the developers of **crewAI** and the contributors to the tools and libraries used in this project.
