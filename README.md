def find_longest_word(file_path):
    try:
        with open(file_path, 'r') as file:
            content = file.read()
            words = content.split()
            longest_word = max(words, key=len)
            return longest_word
    except FileNotFoundError:
        print("File not found.")
        return None
file_path = 'WORDS.txt'  
longest_word = find_longest_word(file_path)

if longest_word:
    print(f"The longest word in the file is: {longest_word}")
