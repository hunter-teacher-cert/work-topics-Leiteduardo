#1. Uncomment the compound_sentence( ) function and add code that randomly generates and joins two independent clauses, using a conjunction.  
#2. Uncomment the complex_sentence( ) function and add code that randomly generates and joins a dependent and an independent clause.
#3. Uncomment the compound_complex_sentence( ) function and add code that randomly generates and joins a dependent clause with an independent clause, a conjunction, and an independent clause.


import random

articles = ["a", "the", "one", "some"]
nouns = ["apple", "carrot", "rabbit", "banana", "basketball", "chess", "sun", "wind"]
verbs = ["cooks", "blows", "bounces", "walks", "jumps", "calls", "stays", "runs", "abides"]
conjunctions = ["for", "and", "nor", "but", "yet", "so"]
dependent_clause_markers = ["although", "even if", "until", "when", "whether", "while", "in order to"]

def independent_clause():
    return random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs)

def dependent_clause():
    return random.choice(dependent_clause_markers) + " " + independent_clause()

def simple_sentence():
    return independent_clause() + "."

def compound_sentence():
    return random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs) + " " + random.choice(conjunctions) + " " +  random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs)
def complex_sentence():
   return random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs) + " " +random.choice(dependent_clause_markers) + " "   + random.choice(nouns) + " " + random.choice(verbs)
def compound_complex_sentence():
   return random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs) + " " +random.choice(dependent_clause_markers) + " "   + random.choice(nouns) + " " + random.choice(verbs) + " " + random.choice(conjunctions) + " " + random.choice(articles) + " " + random.choice(nouns) + " " + random.choice(verbs)
if __name__ == "__main__":
    #test print for simple sentence
    sentence = simple_sentence()
    print(sentence)
    # #test print for compound sentence
    compound_sentence = compound_sentence()
    print(compound_sentence)
    # #test print for complex sentence
    complex_sentence = complex_sentence()
    print(complex_sentence)
    # #test print for compound-complex sentence
    compound_complex_sentence = compound_complex_sentence()
    print(compound_complex_sentence)
