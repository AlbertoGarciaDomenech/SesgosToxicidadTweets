# Guía csv
Estos archivos csv se generaron modificando los tweets proporcionados por Newtral y viendo su toxicidad "toxic" y "very toxic" según su modelo "finetuned-toxic-political-tweets-es"
## tweet_mods_political_parties_[PARTY]_.csv
    twitter_id: identificador del tweet
    original_text: texto del tweet original	
    slug: nombre del político que twitteó	
    party_slug: partido del político que twitteó	
    party_original: string original que se va a sustituir - nombre de un partido ([PARTY])	
    toxic_original: toxicidad “toxic” del tweet original	
    very_toxic_original: toxicidad “very toxic” del tweet original		
    most_toxic_party: string que corresponde con un partido que, al sustituir [PARTY] por él en el tweet, da más toxicidad “toxic” 	
    most_toxic_party_toxicity: toxicidad “toxic” que da el tweet modificado cambiando [PARTY] por most_toxic_party
    most_verytoxic_party:  string que corresponde con un partido que, al sustituir [PARTY] por él en el tweet, da más toxicidad “very toxic” 		
    most_verytoxic_party_toxicity:  toxicidad “very toxic” que da el tweet modificado cambiando [PARTY] por most_toxic_party
    PARTIDO_toxic:  toxicidad “toxic” que da el tweet modificado cambiando [PARTY] por la palabra “partido”	
    PARTIDO_verytoxic: toxicidad “very toxic” que da el tweet modificado cambiando [PARTY] por la palabra “partido”	

## tweet_mods_politicians.csv

## tweet_mods_fascism_communism.csv

    twitter_id: identificador del tweet
    original_text: texto del tweet original	
    slug: nombre del político que twitteó	
    party_slug: partido del político que twitteó	
    comuni_toxic: toxicidad “toxic” del tweet con la palabra comunista/comunismo
    comuni_very_toxic: toxicidad “very toxic” del tweet con la palabra comunista/comunismo
    fascis_toxic: toxicidad “toxic” del tweet con la palabra fascista/fascismo
    fascis_very_toxic: toxicidad “very toxic” del tweet con la palabra fascista/fascismo
    most_toxic: de las dos palabras (fascista/comunista o fascismo/comunismo), cuál hace que el tweet de más toxicidad “toxic”
    most_very_toxic: de las dos palabras (fascista/comunista o fascismo/comunismo), cuál hace que el tweet de más toxicidad “very toxic”

## tweet_mods_accents.csv
	
    twitter_id: identificador del tweet
	original_text: texto del tweet original	
	slug: nombre del político que twitteó	
	party_slug: partido del político que twitteó	
    toxic_original: toxicidad “toxic” del tweet original con tildes
    very_toxic_original: toxicidad “very toxic” del tweet original con tildes
    toxic_noaccent: toxicidad “toxic” del tweet modificado sin tildes
    very_toxic_noaccent: toxicidad “very toxic” del tweet modificado sin tildes
    most_toxic_grammar: ortografía (con tildes/sin tildes) con la que el tweet tiene más toxicidad “toxic”
    most_verytoxic_grammar: ortografía (con tildes/sin tildes) con la que el tweet tiene más toxicidad “very toxic”
