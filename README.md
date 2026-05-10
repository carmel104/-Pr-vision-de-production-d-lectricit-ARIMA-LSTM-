Analyse de la Production d'Électricité aux USA : ARIMA vs LSTM
Ce projet propose une étude comparative entre deux approches de modélisation des séries temporelles : une méthode statistique classique (ARIMA) et une méthode basée sur l'apprentissage profond (LSTM). L'objectif est de modéliser et de prédire la production mensuelle d'électricité aux États-Unis sur la période 1973-2005.

📌 Objectif du Projet
L'enjeu est de capturer les composantes complexes d'une série temporelle réelle — à savoir la tendance (croissance de la demande énergétique) et la saisonnalité (variations climatiques hivernales et estivales) — pour effectuer des prévisions précises.

Le projet se divise en deux volets :

Approche Statistique (R) : Analyse de la stationnarité, identification de l'ordre du modèle et tests de validation.

Approche Deep Learning (Python) : Mise en œuvre d'un réseau de neurones récurrents (RNN) pour apprendre les dépendances temporelles.

📊 Description des Données
Le dataset contient la production mensuelle d'électricité aux USA de janvier 1973 à décembre 2005.

Tendance : Clairement haussière sur le long terme.

Saisonnalité : Pics cycliques correspondant aux périodes de haute consommation.

🛠️ Méthodologie et Modèles
1. Modèle ARIMA (implémenté sous R)
Le processus suit la méthodologie de Box-Jenkins :

Stationnarisation : Utilisation de la différenciation pour stabiliser la moyenne et la variance (test ADF et KPSS).

Identification : Analyse des fonctions d'autocorrélation (ACF) et d'autocorrélation partielle (PACF).

Modèle retenu : ARIMA(2,1,3).

Validation : Absence d'autocorrélation des résidus (Test de Box-Ljung) et validation de l'homoscédasticité.

2. Modèle LSTM (implémenté sous Python/TensorFlow)
Le modèle Long Short-Term Memory est utilisé pour surpasser les limites des modèles linéaires :

Architecture : Une couche LSTM suivie d'une couche Dense (Dense output).

Prétraitement : Normalisation des données avec MinMaxScaler.

Performance : -   Perte entraînement (MSE) : 0.0165

Perte test (MSE) : 0.0147

Conclusion technique : Absence de surajustement (overfitting) et bonne capacité de généralisation.

🚀 Structure du Dépôt
Plaintext
├── R_Analysis/
│   └── script_arima.R      # Code pour la modélisation ARIMA et tests statistiques
├── Python_ML/
│   └── lstm_model.ipynb    # Notebook pour le réseau de neurones LSTM
├── Data/
│   └── electricity_usa.csv # Dataset source (01/1973 - 12/2005)
└── README.md
📈 Résultats
ARIMA s'est révélé extrêmement efficace pour capturer la structure saisonnière grâce à sa rigueur mathématique.

LSTM a montré une grande flexibilité, bien qu'il puisse être encore amélioré par l'ajustement plus fin des hyperparamètres (learning rate, nombre d'unités).

👥 Auteurs
AWANDE Carmel

AYONOU Antoine

GANDJI Edmond

Projet réalisé dans le cadre du Master 2 Statistique Appliquée aux Vivants (CIPMA - Chaire UNESCO).
