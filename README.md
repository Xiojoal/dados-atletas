# dados-atletas
Indica dados pessoais do atleta com IMC, categoria e média
// Classe Atleta
class Atleta {
    constructor(nome, idade, peso, altura, notas){
       this.nome = nome;
       this.idade = idade;
       this.peso = peso;
       this.altura = altura;
       this.notas = notas;
    }
// De acordo com as idades, a categoria do atleta é indicada 
calcularCategoria() {
    if (this.idade >= 8 && this.idade <= 11)
            return "Infantil"
        if (this.idade >= 12 && this.idade <= 13)
            return "Juvenil"
        if (this.idade >= 14 && this.idade <= 15)
            return "Intermediario"
        if (this.idade >= 16 && this.idade <= 30)
            return "Adulto"
         if (this.idade > 30)
         return "Sem Gategoria"   
    }
//  Para calcular o IMC   
    calcularIMC() {
        return this.peso / (this.altura * this.altura)
    }
// Para calcular a média válida
calcularMediaValida() {
  this.notas = this.notas.sort();
  this.notas = this.notas.slice(1, 4);
  let soma = this.notas.reduce(function(total, atual){
  return total + atual
 }, 0);
 let mediaValida = (soma / this.notas.length);
 return mediaValida;
}
//Método nome Atleta
   obtemNomeAtleta(){
    return this.nome;
}
//Método Idade Atleta
    obtemIdadeAtleta(){
        return this.idade;
    } 
    //Método Peso Atleta
    obtemPesoAtleta() {
        return this.peso;
    } 
    //Método Altura Atleta
     obtemAlturaAtleta() {
        return this.altura;
    } 
  //Método Notas Atleta
    obtemNotasAtleta() {
        return this.notas;
    } 
  //Método Categoria Atleta
    obtemCategoria() {
        return atleta.calcularCategoria()
    } 
  //Método IMC Atleta
    obtemIMC() {
        return atleta.calcularIMC()
    } 
    //MétodoMétodo de classificação média do atleta Atleta
    obtemMediaValida() {
        return atleta.calcularMediaValida()
    }
}

const atleta = new Atleta("Cesar Abascal",30, 80, 1.70, [10, 9.34, 8.42, 10, 7.88]);

console.log("Nome: " + atleta.obtemNomeAtleta());// Retorna o nome do atleta
console.log("Idade: " + atleta.obtemIdadeAtleta());// Retorna a idade do atleta
console.log("Peso: " + atleta.obtemPesoAtleta());// Retorna o peso do atleta
console.log("Altura: " + atleta.obtemAlturaAtleta());// Retorna a Altura do atleta
console.log("Notas: " + atleta.obtemNotasAtleta());// Retorna as notas do atleta
console.log("Categoria: " + atleta.obtemCategoria());// Retorna a categoria do atleta
console.log("IMC: " + atleta.obtemIMC());// que retorna o IMCo atleta
console.log("Media: " + atleta.calcularMediaValida());// que retorna a média válida do atleta
//Utilize as seguintes regras:
console.log("-----");









