# Adaptive-Model-Switching-in-AWS-SageMaker

This project tackles the challenge of building trust and agility within machine learning (ML) pipelines deployed on AWS SageMaker. Traditionally, deploying new models can be risky and user confidence can be low due to a lack of transparency.

To address this, the project leverages several key techniques:
Guardrails with Canary Deployments and Automatic Rollbacks: New models are introduced to a small portion of traffic first (canary group), allowing for early detection of issues. If the canary model underperforms, the system automatically rolls back to the previous stable version, minimizing downtime and impact on users.

Shadow Testing for Continuous Evaluation: New models are evaluated in parallel with the production model on a subset of live traffic. Their predictions aren't used for decisions, but their performance is compared. This allows for continuous evaluation without affecting production and empowers informed model selection.

Transparency for User Confidence: The project tackles the historical lack of transparency by providing clear visibility into user activity monitoring and the rationale behind model selection decisions. This fosters trust in the models and the overall ML pipeline.

By implementing these techniques, the project aims to significantly increase user confidence (by 75-80%) in the ML models. Users can be assured that new models are deployed reliably, continuously evaluated, and chosen through a transparent process. 
