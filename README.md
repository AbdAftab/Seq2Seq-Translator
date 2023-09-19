# French to English Translator Built Using Seq2Seq
Heavily inspired by Aladdin Persson's German to English Translator.

The goal of this project was to implement the Seq2Seq model while also understanding the paper behind it. Additionally, I used this project to deepen my knowledge and understanding of PyTorch, LSTM's, and NLP in general.

For most of these tests, we used the sentence **"une femme française moyenne mange une pomme"**, which roughly translates to **"an average woman eats an apple"**. Below, we will be able to see some "key" epochs where the model improved or understood something new.

## Epoch 0/100
Below, we can see that there's no real direction or real understanding of language within our model. The words here don't really have any correlation to our target sentence.
![image](https://github.com/AbdAftab/Seq2Seq-Translator/assets/57965010/52509361-14fc-4790-a6e8-015d1c9173e7)

## Epoch 1/100
Immediately after the first epoch, we can see a massive improvement with our model being able to extract **"A woman is"**, but then begins to repeat itself

![image](https://github.com/AbdAftab/Seq2Seq-Translator/assets/57965010/14d2f3a7-f177-4d02-861e-bdc976fe6dbf)

## Epoch 20/100
Here, we can see that our model is now translating a little bit more. It now is translating **"a woman is eating"**. Pretty cool :)
![image](https://github.com/AbdAftab/Seq2Seq-Translator/assets/57965010/ad6ef624-b71e-49d3-98a7-1ed1557f3240)

## Epoch 30/100
Here, we get that a woman is eating a chip, which is wrong but at least it's giving her an edible object to eat :)

![image](https://github.com/AbdAftab/Seq2Seq-Translator/assets/57965010/3bf573ec-52d4-4242-93ba-bf3a09db3b9a)

After Epoch 30, I didn't see much improvement (other than the <unk> token being removed at some point).


## Another Sentence Sample Test
Using a version of the model that was stopped at ~50 epochs in, I fed it a new sentence, **"La femme répare sa maison"**. In English, this means **"The woman is fixing her home"** to which the model translated:
![image](https://github.com/AbdAftab/Seq2Seq-Translator/assets/57965010/796ceaa3-ae34-4a4a-9216-d773237a52ee)

Ended up doing pretty good on this example, but performance still varies.
