# water_data_analysis

In this project of water and soil analysis i Had taken data from two different csv fill

But i was instruted that to take the data from api so i had convert the water data into api format by using Flask library 

code is given below

pip install Flask pandas
from flask import Flask, jsonify
import pandas as pd

app = Flask(__name__)
df = pd.read_csv('water_data.csv')
@app.route('/api/water-data', methods=['GET'])
def get_water_data():
    # Convert DataFrame to JSON
    water_data_json = df.to_json(orient='records')
    return jsonify(water_data_json)
if __name__ == '__main__':
    app.run(debug=True)
python app.py

And you can see the fill at zip fill as  real.ipynb
