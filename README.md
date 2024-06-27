# Italian-quiz
translations = {
        "hello": "ciao",
        "today": "oggi",
        "free": "libero",
        "please": "perfavore",
        "goodbye": "arrivederci",
        "friend": "amico",
        "tomorrow": "domani",
        "man": "uomo",
        "who": "chi",
        "all": "tutto"
    }


def quiz():
    correct_answers = 0
    #starts off as 0 will increase based on user points accumulated
    total_questions = len(translations)
    #len is grabbing info from translations wordbox 
    print("Welcome to your Italian quiz!")
    print("Translate the following words into Italian:")
    print()
    for english_word, italian_translation in translations.items():
        user_translation = input(f"What is the Italian translation of '{english_word}'? ")
        
        if user_translation.lower() == italian_translation.lower():
            print("That is correct!")
            correct_answers += 1
        else:
            print(f"That is incorrect, the correct Italian translation for '{english_word}' is '{italian_translation}'.")
        
        print()
         
    
    print(f"You got {correct_answers}/{total_questions} words correct.")
    if correct_answers == total_questions:
        print("Perfect! or should i say, Perfetto!")
    elif correct_answers > total_questions * 0.8:
        print("Great job! Lets try to get a perfect score.")
    else:
        print("Keep practicing for a better score.")


quiz()
