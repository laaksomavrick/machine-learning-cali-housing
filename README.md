# machine-learning-cali-housing

Working through the "Hands-on Machine Learning" (Aurelien Geron) book, and as such, attempting to build a machine learning model of California real estate prices as per a 1990's dataset.

References (e.g. notebooks) come from this repository:
* https://github.com/ageron/handson-ml3

## Dependencies

* `python` >= 3.10
* `poetry`

I also had to run `brew install openblas` and export some shell flags on my M1 mac. See [this](https://stackoverflow.com/a/70178471/4198382) StackOverflow answer for details.

## Our goal

Build a model that given a particular district's features can predict the median housing price of that district

## The data scientist checklist

- [ ] Frame the problem and look at the big picture
- [ ] Retrieve the data
- [ ] Explore the data to gain insights
- [ ] Prepare the data to better expose the underlying patterns as they relate to machine learning algorithms
- [ ] Explore many different models and shortlist the best ones
- [ ] Fine-tune your models and combine them into a great solution
- [ ] Present your solution
- [ ] Launch, monitor, and maintain your system

### Framing the problem

#### What kind of machine learning system?

* We want to use supervised learning given we have labeled examples (district features and their median price).
* This is a regression task, meaning we want to predict a value given a set of features.
* Batch learning is acceptable given 1) we have no continuous data flow and 2) the data set is relatively small (can fit into memory). Moreover, the data does not change frequently.

#### What is the performance measure?

* Root mean square error (RMSE), which is a typical performance measure for regression problems (I am taking this as a given).