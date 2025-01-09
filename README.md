# sagemaker-mme-with-djl
 Cost efficient and robust machine learning inference with Amazon SageMaker multi-model endpoints

This blogpost builds on and extends the excellent blogpost published in February 2024 called “Run ML inference on unplanned and spiky traffic using Amazon SageMaker multi-model endpoints”. The architecture outline and key points in that blogpost remain valid and I recommend you reading that in conjunction with this article.
 
What different and new with this article is 1/ there is more of an emphasis on the working example to help you more easily translate your use case to this solution, such as showing the simultaneous use of different model classes, and 2/ the working example works (where the original worked example no longer works due the platform/library version updates).
 
As noted in the original article: With this architecture, a software as a service (SaaS) business can break the linearly increasing cost of hosting multiple models and achieve reuse of infrastructure consistent with the multi-tenancy model applied elsewhere in the application stack. 

This solution uses DJL Serving with an Amazon SageMaker MME, as a result the configuration differs from the default MME setup. This is described in the base blogpost. The change is not onerous and benefits are many, including being able to readily deploy multiple native Scikit Learn models to the same endpoint. This is what is demonstrated in the accompanying code.
 