# Guía csv
Estos archivos csv se generaron modificando los tweets proporcionados por Newtral u obteniendo tweets nuevos, y viendo su toxicidad "toxic" y "very toxic" según su modelo "finetuned-toxic-political-tweets-es"
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
    most_verytoxic_party_toxicity:  toxicidad “very toxic” que da el tweet modificado cambiando [PARTY] por most_verytoxic_party
    PARTIDO_toxic:  toxicidad “toxic” que da el tweet modificado cambiando [PARTY] por la palabra “partido”	
    PARTIDO_verytoxic: toxicidad “very toxic” que da el tweet modificado cambiando [PARTY] por la palabra “partido”	

## tweet_mods_politicians.csv

    twitter_id: identificador del tweet
    original_text: texto del tweet original	
    slug: nombre del político que twitteó	
    party_slug: partido del político que twitteó	
    original_name: string original que se va a sustituir - nombre de un politico
    toxic_original: toxicidad “toxic” del tweet original	
    very_toxic_original: toxicidad “very toxic” del tweet original		
    most_toxic_leader: string que corresponde con un nombre de un politico o un arroba que, al sustituir original_name por él en el tweet, da más toxicidad “toxic” 	
    most_toxic_leader_toxicity: toxicidad “toxic” que da el tweet modificado cambiando original_name por most_toxic_leader
    most_verytoxic_leader:  string que corresponde con un nombre de un politico o un arroba que, al sustituir original_name por él en el tweet, da más toxicidad “very toxic” 	
    most_verytoxic_leader__toxicity:  toxicidad “very toxic” que da el tweet modificado cambiando original_name por most_toxic_leader
    LIDER_TOXIC:  toxicidad “toxic” que da el tweet modificado cambiando original_name por la palabra “lider”	
    LIDER_verytoxic: toxicidad “very toxic” que da el tweet modificado cambiando original_name por la palabra “lider”	
    
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
    
## tweets_contradictorios.csv
    tweets: tweet con contenido tanto tóxico como no tóxico, para comprobar el comportamiento del modelo ante estos casos
    manual_toxicity: valor manual asignado al tweet (1- tóxico; 0 - no tóxico)
    predicted_toxic: toxicidad "toxic" del tweet
    predicted_verytoxic: toxicidad "very toxic" del tweet
    predicted_toxic_value: valor entre 0 y 2 que indica toxicidad "toxic" (2 - muy tóxico; 1 - tóxico; 0 - no tóxico)	
    predicted_verytoxic_value: valor entre 0 y 2 que indica toxicidad "very toxic" (2 - muy tóxico; 1 - tóxico; 0 - no tóxico)

## tweet_mods_emojis.csv

    twitter_id: identificador del tweet
    original_text: texto del tweet original	
    slug: nombre del político que twitteó	
    party_slug: partido del político que twitteó	
    emojis: emojis que aparecen en el tweet	
    toxicity: toxicidad “toxic” del tweet original	
    toxicity_without_emoji: toxicidad “toxic” del tweet sin los emojis		
    sev_toxicity: toxicidad “very toxic” del tweet original	
    sev_toxicity_without_emoji: toxicidad “very toxic” del tweet sin los emojis
   
## tweet_mods_emojis2.csv

    emoji: identificador del emoji
    count:  numero de veces que aparece el emoji	
    total_toxicity: sumatorio de toxicidad "toxic" del emoji	
    mean: media de toxicidad "toxic"
    most_toxic: tweet con mayor toxicidad "toxic" donde aparece el emoji
    most_toxic_text: texto del tweet con mayor toxicidad "toxic"
    
## tweet_mods_emojis_replace.csv

    previous_emoji: identificador del emoji original
    original_text: texto del tweet original	
    toxicity: toxicidad "toxic" del tweet original	
    emplaced_emoji: identificador del nuevo emoji	
    text_replaced: texto del tweet con el nuevo emoji	
    toxicity_replaced: toxicidad “toxic” del tweet con el nuevo emoji	
