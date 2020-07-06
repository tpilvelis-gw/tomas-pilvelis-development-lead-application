# 5 Metric Visualisations for a Serverless Product


## 1. Number of requests made due to bad parameters inserted


This would be a great indication of <b>ease of use</b> to the user of the product. 

I would say that if the user has managed to find, copy, paste code. Insert API Key and all other parameters correctly all in one attempt to make an API call. This is a good metric to determine <b>usability</b> and <b>quality of documentation</b>.


## 2. Number of Cold Starts


This can be avoided if running hot constantly. However if this had to be the case. It can significantly affect performance of the end user application. Consider the end user may have <b>non functional</b> requirements they have to meet. The less cold starts the more performant the product is.


## 3. Errors


Errors can occour for many reasons or combinations. This can be frustrating to the end user and whilst a response stating the error is great and completes the feedback loop. It would be good to avoid. Depending on the error they can be hard to overcome however effort must be made to avoid this. Unhandled exceptions.


## 4. Duration


Duration allows us to monitor the performance of the product. Time is money in the world of Serverless, so reducing execution time to <b>reduce cost</b> where possible should be considered a priority.

## 5. 


## Excluded Metrics


I would argue invocations is irrelivant. A successful product should not need to monitor this figure. Yes it is a good metric, however a rough correlation can be found by purchases.

If we could be cheeky, I would have said there is a one-to-one relationship with duration and invocations. Each invocation will have a duration so a metric could be derived from this.

