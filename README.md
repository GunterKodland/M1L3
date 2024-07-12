# M1L3
from flask import Flask 
import random

app = Flask(__name__)

lista_consejos=["La mayoría de las personas que sufren adicción tecnológica experimentan un fuerte estrés cuando se encuentran fuera del área de cobertura de la red o no pueden utilizar sus dispositivos",
                "Según un estudio realizado en 2018, más del 50% de las personas de entre 18 y 34 años se consideran dependientes de sus smartphones.",
                "Según un estudio de 2019, más del 60% de las personas responden a mensajes de trabajo en sus smartphones en los 15 minutos siguientes a salir del trabajo"]

@app.route("/")
def Consejos():
    return f'<p>{random.choice(lista_consejos)}</p>'

app.run(debug=True)
