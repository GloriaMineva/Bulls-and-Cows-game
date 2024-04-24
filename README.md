# Bulls-and-Cows-game
secret_number = '5372'
counter = 0
print('My secret number is with 4 different digits from 1 to 9.\
 You have 10 attempts to find it! Good luck!')
while True:
    player_number = input('Can you guess my secret number...')
    if secret_number == player_number:
        print('Congratulations! You win!')
        break
    else:
        counter += 1
        bull = 0
        cow = 0
        if player_number[0] == secret_number[0]:
            bull += 1
        else:
            for i in secret_number:
                if i == player_number[0]:
                    cow += 1
        if player_number[1] == secret_number[1]:
            bull += 1
        else:
            for j in secret_number:
                if j == player_number[1]:
                    cow += 1
        if player_number[2] == secret_number[2]:
            bull += 1
        else:
            for k in secret_number:
                if k == player_number[2]:
                    cow += 1
        if player_number[3] == secret_number[3]:
            bull += 1
        else:
            for l in secret_number:
                if l == player_number[3]:
                    cow += 1
        print(f'You have {bull} bulls and {cow} cows.')

    if counter >= 10:
        print('Sorry! You have no more attempts and you loose!')
        break




