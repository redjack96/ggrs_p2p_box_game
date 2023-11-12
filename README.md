# GGRS p2p example
Baseline for a peer-to-peer multiplayer game using bevy 0.12.0 and bevy_ggrs

# Run
Each player should use a different local port, and should have all the other players's addresses 

    cargo run --package ggrs_p2p_box_game --bin box_game_p2p -- --local-port 7000 --players localhost 127.0.0.1:7001
    cargo run --package ggrs_p2p_box_game --bin box_game_p2p -- --local-port 7001 --players 127.0.0.1:7000 localhost

# Copiare il file con scp:


  scp ./prova.txt  valter@192.168.1.13:~/Scambio/prova.txt

# TODO
- Lobby system to avoid listing all the addresses. 
  - The first player is the host, the others joins the lobby.
  - The first player waits for other player join the lobby.
  - Repeat for each player: when a player joins the lobby, it sends its name the the host. The host will send its name to the guest.
  - Each guest and the host can send a "I'm ready" message, so that the host has the ability to start the game
  - When there are at least two players, the host can start the game.
- there should be a fixed maximum number of players (?)
- 
