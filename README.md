# Keystroke dynamics patterns while writing positive and negative opinions

This repository cantains dataset referred in the following article:

Kołakowska, Agata, and Agnieszka Landowska. 2021. "Keystroke Dynamics Patterns While Writing Positive and Negative Opinions" Sensors 21, no. 17: 5963. https://doi.org/10.3390/s21175963 

The repository contains data collected in 2017 in order to perform an experiment in which keystroke dynamics patterns were analyzed while writing various opinions. The participants were asked to write opinions on their worst and best learning experience, while all keystrokes were captured. The research question of the study might be given as follows: Is there any difference in keystroke dynamics patterns while writing positive and negative opinions.

The **data.csv** file contains feature vectors extracted on the basis of raw data. There are 245 vectors (rows) containing 51 features (columns). For each of 49 participants 5 feature vectors were extracted (5 x 49 = 245):  

1. vector extracted on the basis of all keestrokes generated by a user during the experiment session  
2. vector extracted on te basis of keystrokes generated by a user while writing an opinion on the best teacher (positive opinoin) 
3. vector extracted on te basis of keystrokes generated by a user while writing an opinion on the worst teacher (negative opinion) 
4. vector extracted on te basis of keystrokes generated by a user while writing an opinion on the best subject (positive opinion) 
5. vector extracted on te basis of keystrokes generated by a user while writing an opinion on the worst teacher (negative opinion) 

Every successive five vectors belong to the next participant of the experiment.

The columns headers indicate the type of feature. The list below presents the features. Most features are mean values and standard deviation denoted
as [0] and [1] respectively.

- di_1D2D[0], di_1D2D[1]  - duration between the 1st and the 2nd down keys of a digraph
- di_1Dur[0], di_1Dur[1]  - duration of the 1st key of a digraph
- di_1KeyLat[0], di_1KeyLat[1] - duration between the 1st key up and the next key down of a digraph
- di_2Dur[0], di_2Dur[1] - duration of the 2nd key of a digraph
- di_Dur[0], di_Dur[1] - duration of the whole digraph from the 1st key down to the last key up
- di_NumEvents[0], di_NumEvents[1] number of key events for a digraph
- tri_1D2D[0], tri_1D2D[1] duration between the 1st and the 2nd down key of a trigraph
- tri_1Dur[0], tri_1Dur[1] duration of the 1st key of a trigraph
- tri_1KeyLat[0], tri_1KeyLat[1] duration between the 1st key up and the next key down of a trigraph
- tri_2D3D[0], tri_2D3D[1] duration between the 2nd and the 3rd down key of a trigraph
- tri_2Dur[0], tri_2Dur[1] duration of the 2nd key of a trigraph
- tri_2KeyLat[0], tri_2KeyLat[1] duration between the 2nd key up and the next key down of a trigraph
- tri_3Dur[0], tri_3Dur[1] duration of the third key of a trigraph
- tri_Dur[0], tri_Dur[1] duration of the whole trigraph from the 1st key down to the last key up
- tri_NumEvents[0], tri_NumEvents[1] number of key events for a trigraph Shift digraph features
- L_di_1D2D[0], L_di_1D2D[1] time between pressing the 1st and the 2nd key in a digraph starting from the left shift
- L_di_Dur[0], L_di_Dur[1] duration of a digraph starting from the left shift (time between pressing the 1st and releasing the 2nd key)
- L_first_shift_up percentage of time when the left shift starting a digraph is released before releasing the 2nd key
- R_di_1D2D[0], R_di_1D2D[1] time between pressing the 1st and the 2nd key in a digraph starting from the right shift
- R_di_Dur[0], R_di_Dur[1] duration of a digraph starting from the right shift (time between pressing the 1st and releasing the 2nd key)
- R_first_shift_up percentage of time when the right shift starting a digraph is released before releasing the 2nd key
- SPACE frequency of using spacebar
- BACKSPACE frequency of using backspace key
- DEL frequency of using delete key
- UP frequency of using up arrow
- DOWN frequency of using down arrow
- LEFT frequency of using left arrow
- RIGHT frequency of using right arrow
- SHIFT_L frequency of using left shift
- SHIFT_R frequency of using right shift
- CAPS frequency of using caps lock
- SPEED average number of keystrokes per second


The **labels.csv** file contains PAD (Pleasure, Arousal, Dominance) labels reported at specified moments of the experiment session. Each user reported the emotional state five times so there are 5 vectors for each users. It gives 245 rows, each containing 3 values. The pleasure, arousal, dominance were all reported using a 9-point Likert scale. In the case of pleasure and arousal the lower the value the state is more positive or more aroused respectively. In the case od dominance the lower the value the less dominant affective state. Every successive five vectors belong to the next participant of the experiment. The vectors for each user are given in the following order:

1. PAD values reported at the beginning of the session
2. PAD values reported after writing a positive opinion on a teacher
3. PAD values reported after writing a negative opinion on a teacher
4. PAD values reported after writing a positive opinion on a subject
5. PAD values reported after writing a negative opinion on a subject 
