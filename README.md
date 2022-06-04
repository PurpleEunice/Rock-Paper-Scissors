import random

my_score = 0
comp_score = 0


for i in range(0, 9):

    choices = ('rock', 'paper', 'scissors')
    comp_choices = choices[random.randint(0, 2)]
    my_choices = input('Rock, Paper or Scissors? Your choice:  ').lower()

    win_combos = [
        ['rock', 'scissors'],
        ['scissors', 'paper'],
        ['paper', 'rock']
    ]

    decide_win = [my_choices, comp_choices]

    if my_choices == comp_choices:
        my_score += 1
        comp_score += 1
        print(decide_win)
        print(f'You: {my_choices} -- Computer: {comp_choices} -- Verdict: Draw')
        print(f'You: {my_score} - {comp_score}')
    elif decide_win == win_combos[0] or decide_win == win_combos[1] or decide_win == win_combos[2]:
        my_score += 1
        print(decide_win)
        print(f'You: {my_choices} -- Computer: {comp_choices} -- Verdict: You win')
        print(f'{my_score} - {comp_score}')
    else:
        comp_score += 1
        print(decide_win)
        print(f'You: {my_choices} -- Computer: {comp_choices} -- Verdict: You Lose!')
        print(f'{my_score} - {comp_score}')
