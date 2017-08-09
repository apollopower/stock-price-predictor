# Stock Price Predictor Graph

This is a program that generates three predictive models to estimate the
future price of a given stock. Note that this was only built as an
exercise in getting a better understanding of Python and Data Science.

## How to Use This Program

In order to analyze data about a specific stock properly, we will need to:

- Install the dependencies for this program
- Insert our desired dataset in the form of a CSV file
- Execute the program and generate our graph

### Dependencies 

This Stock Price Predictor relies on several modules, and runs on Python3

- Python3: If you do not have it running on your machine, [find out how here](https://www.python.org/downloads/)

Once you have Python3 set up on your machine, install the following dependencies:

- CSV: This will allow us to read data from the CSV file of our given stock
- Numpy: A linear algebra library that will manipulate our data
- Scikit-learn: We use this to generate our predictive models
- Matplotlib is used to visualize our models and plot our data

You cann install all of them by running these commands:

```bash
pip install install csv
pip install install numpy
pip install install scikit-learn
pip install install matplotlib
```

### Choosing our Dataset

Already included in this repo are two data sets, one for Apple and one for Amazon.
However, you can input your own by downloading a CSV from the past 30 days worth
of stock prices from a particular company on [Google Finance](https://www.google.com/finance)

Include the CSV file under the same directory as the ```predictor.py``` file, and
on line 40 of the script, insert the file name like so:

```python
get_data('YOUR_FILE_HERE')
```

The Apple stock is included as an example.

### Executing the Program

To run the script, simply input into your command line:

```bash
python predictor.py
```

If a graph is not generated after running this command (It may take some time),
insert this line into the beginning of the script, right after the imports:

```python
plt.switch_backend('NEW_BACKEND_HERE') 
```

Where it says "NEW_BACKEND_HERE", replace that with different options your command
prompt will suggest to you until the appropriate graph tool is implemented.

On most machines, you SHOULD NOT have this issue.

Now your graph will generate with our three predicitve models. You can now see what
model is most accurate and should help you make more sound financial investments!
(Just don't put all that money into one place! #DIVERSIFY)

## The Magic Under the Hood

As briefly mentioned before, this is an exercise of using Python and Machine
Learning for Data Science. In short, we are generating three predictive models
that are __Support Vector Machines.__

**Support Vector Machines** are supervised learning models in machine learning. They
analyze data that has already been classified, and with *regression analysis*,
learn to classify new sets of data.

In the case of our script, we are training 3 different Support Vector Machines to
predict future stock prices with currently existing ones. Regression Analysis then
lets us project into the future to what possible prices for a given stock may be.

The three models we use are:

- A Linear SVM
- A Polynomial SVM
- A Radial Basis Function (RBF)

SVMs are extensice topics in machine learning, [you can learn more about them here](https://en.wikipedia.org/wiki/Support_vector_machine#Linear_SVM)

## Acknowledgments 

This was a project based on [Siraj Raval's Data Science Lectures and videos.](https://www.youtube.com/channel/UCWN3xxRkmTPmbKwht9FuE5A)
Big thanks to him for democratizing the understanding of AI and machine learning!