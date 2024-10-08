# A Chess Transformer

## Dataset

Data is originally from the [Lichess Elite Database](https://database.nikonoel.fr/). I made use of this [script](https://github.com/sgrvinod/chess-transformers/blob/main/chess_transformers/data/LE22c.sh) from sgrvinod which uses pgn-extract to extract the FENs, moves, and outcomes of the games within the pgn files. Note that the script applies a filter to keep only games that ended in checkmate and that used a time control of at least 5 minutes. 

The dataset consists of 26,701,685 half-moves, the FEN description of the board position that the move was played, and the outcome of the game (1 for win by white and -1 for win by black)

[Download Here](https://drive.google.com/uc?export=download&id=1XuyQCim9l1ia8VG0MVSzYgxpdJa_rEtK)

The dataset contains two tables: data and encoded_data. The data table contains the raw FEN sequences, moves, and outcome of each game. The encoded_data contains the encoded FENs after applying a transformation, encoded moves, and outcome of each game. 

- **`Lichess_Elite_Dataset.h5`** 
    - **data**
        - fen
        - move
        - outcome
    - **encoded_data**
        - encoded_fen
        - encoded_move
        - outcome
