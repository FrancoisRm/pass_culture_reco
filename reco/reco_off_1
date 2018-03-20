from flask import current_app as app
from flask_login import current_user
from sqlalchemy.sql.expression import func

Event = app.model.Event
EventOccurence = app.model.EventOccurence
Mediation = app.model.Mediation
Offer = app.model.Offer
UserMediation = app.model.UserMediation
UserMediationOffer = app.model.UserMediationOffer
Thing = app.model.Thing

def get_recommended_offers(user, limit=3):
    query = Offer.query
    print('before tri offers.count', query.count())
      if user.is_authenticated:
       query = tri(query)


##### DEF FUNCTION TRI

def cluster():
  ordre = Offer.ordre() #renvoie un vecteur avec l'ordre de préférence de types
  query = Offer.query
  query = query.order_by((Thing.type) |
                         (Event.type))
  n = Thing.amount_of_type
  m = Event.amount_of_type
  Thing_type = Thing.list_of_type
  Event_type = Event.list_of_type
  Cluster = [0]*ordre.length

  for i in range(ordre.length()):
    Cluster[i].append(query WHERE query.Thing or Event.type = ordre[i])

  RETURN Cluster 
