- Use config map to load models into vLLM
- Multi-GPU usage
- Use OSSM + Rollouts to upgrade model server/LLM
- Explore LLM Gateway and RHCL use cases
- GitOps deployment
- Instructions for secret creation via CLI



Roll Out strategy
- Canary/Blue-Green for RH AIIS image updates

  Start by deploying a small percentage of the total replica count (e.g., 1 or 2) of the new LLM deployment, keeping the rest of the replicas running the old version. This approach allows you to gradually expose the new version to the live traffic and monitoring its performance.

- A/B Testing for model updates

  When rolling out a new model version, you may want to leverage A/B Testing. A/B Testing allows you to run two or more versions of your LLM simultaneously, serving each version to a portion of the user requests. This way, you can directly compare their performance metrics and choose the best version for your deployment. Keep in mind that this method requires careful monitoring to observe user feedback and errors for each version.