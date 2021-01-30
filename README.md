# codec-proj-11-TeamStats
//A data structure to store the information about our team. Objects section in codec js.

const team = {
  _players: [
    {
     firstName: 'Mike',
     lastName: 'Lopez',
     age: 14,
    },

    {
     firstName: 'Jake',
     lastName: 'Smith',
     age: 15,
    },

    {
     firstName: 'Nick',
     lastName: 'Merlo',
     age: 16,
    }

  ],
  _games: [
    {
      opponent: 'Broncos',
      teamPoints: 42,
      opponentPoints: 27
    },

    {
      opponent: 'Pirates',
      teamPoints: 34,
      opponentPoints: 36
    },

    {
      opponent: 'Mean Machine',
      teamPoints: 46,
      opponentPoints: 42
    }

  ],
  get players() {
    return this._players;
  },

   get games() {
    return this._games;
  },
 
 addPlayer(firstName, lastName, age) {
   let player = {
      firstName: firstName,
      lastName: lastName,
      age: age
   };
   this.players.push(player);
  },
  addGame(oppName, points, oppPoints) {
    const game = {
      opponent: oppName,
      points: points,
      oppPoints: oppPoints
    }
    this.games.push(game);
  }
}

team.addPlayer('Steph', 'Curry', 28);
team.addPlayer('Lisa', 'Leslie', 44);
team.addPlayer('Bugs', 'Bunny', 76);

//console.log(team.players)

team.addGame('Blazerz', 47, 32);
team.addGame('Fryers', 43, 21);
team.addGame('Cracks', 53, 64);

console.log(team.games);



