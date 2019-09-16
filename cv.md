**My name** Bakanov Ilya Sergeevich  

**My mail** is nextdesusu@gmail.com, other way to cantact me is by call me, my phone number is +79171498969  

**My goal** here is to learn how to work with a team and understand what kind of skills my potential employer may need. I however do have some troubles with github for example and some others, so find this training useful.  

**My skills** i know syntax of js, html, css and familiar with some of frameworks such as react.js, express.js, etc... Also i'm familiar with python and c++ syntax and django framework for python.  

**Code examples** This is my solution of love triangles, i thought it can be good example of my code because, its related to rsschool.  

```js
module.exports = function getLoveTrianglesCount(preferences = []) {
    let pairCounter = 0, inLove = {};
    for (let i = 0; i < preferences.length; i++){
        let a = preferences[i], b = preferences[a - 1], c = preferences[b - 1];
        if (preferences[c - 1] === a && (a != b && a != c && b != c) && !inLove[a] && !inLove[b] && !inLove[c]){
            ++pairCounter;
            inLove[a] = true;
            inLove[b] = true;
            inLove[c] = true;
        }
    }
    return pairCounter;
};
```

Next example is a simple assembler interpreter and a solution of one task from codewarriors

```js
function tokenize(sign){
  if (!isNaN(Number(sign))){
    return Number(sign);
  }
  return sign;
}
function simple_assembler(program, context) {
  let output = context || {}, commands, key, val1, val2;
  for (let i = 0; i < program.length; i++){
    commands = program[i].split(' ');
    key = commands[0], val1 = tokenize(commands[1]), val2 = tokenize(commands[2]);
    if (key === "mov"){
      if (typeof val2 === "string"){
        output[val1] = output[val2];
      } else {
        output[val1] = val2;
      }
    } else if (key === "inc"){
      ++output[val1];
    } else if (key === "dec"){
      --output[val1];
    } else if (key === "jnz"){
      if (output[val1] !== 0){
        i += val2 - 1;
      }
    }
  }
	return output;
};
```

Other examples can be finded in my github repositories.