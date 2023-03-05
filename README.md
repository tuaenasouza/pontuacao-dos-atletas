function mediaDasNotas(matrizNomesENotas){

  return matrizNomesENotas.map(function(atleta){
   
    atleta.notas = atleta.notas.sort(function(a, b){return b - a})
    console.log(atleta.notas)

    let notasComputadas = atleta.notas.slice(1,4)
    console.log(notasComputadas)

    let soma = 0
   
    notasComputadas.forEach(function(nota){
      soma = soma + nota
    })

    return `Atleta: ${atleta.nome}
Notas Obtidas: ${atleta.notas}
Média Válida: ${soma/notasComputadas.length}`;
  }).join(`

`)
}

//exemplo de uso

let atletas = [
 {
   nome: "Cesar Abascal",
   notas: [10, 9.34, 8.42, 10, 7.88]
 },
 {
   nome: "Fernando Puntel",
   notas:  [8, 10, 10, 7, 9.33]
 },
 {
   nome: "Daiane Jelinsky",
   notas: [7, 10, 9.5, 9.5, 8]
 },
 {
   nome: "Bruno Castro",
   notas: [10, 10, 10, 9, 9.5]
 }
];

console.log(mediaDasNotas(atletas))