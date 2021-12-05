# Codigo-Java
Repositorio criado para adicionar o codigo Java

Infelizmente o programa não foi terminado, a seguir é apresentado o progresso realizado.

link para download: https://1drv.ms/u/s!AqToD8FMiyjxzAd6iCNzrS9nndqh?e=5qKGz6


import java.util.Scanner;
public class Main {

	public static void main(String[] args) {
		int opt = 0; //opção do usario para acessar o menu
		   Scanner Scan = new Scanner(System.in);
		System.out.println("			CLASH OF YOUTUBERS");
		System.out.println("");
		System.out.println("	MENU");
		System.out.println("1: Inciar Jogo");
		System.out.println("2: Informações do desenvolvededor");
		System.out.println("3: Como Jogar");
		System.out.println("4: Sair");
		opt = Scan.nextInt();
		
		
		switch(opt) {
		case 1: 
			Jogador jogador1 = new Jogador();
			jogador1.iniciarJogador();
			Jogador jogador2 = new Jogador();
			jogador2.iniciarJogador();
			personagem Atila = new personagem("Atila Iamarino", false, "Biologia", 100);
			personagem Pirula = new personagem("Pirula", false, "Paleontologia", 100);
			personagem Castanhari = new personagem("Felipe Castanhari", false, "Historia", 100);	
			personagem Ibere = new personagem("Ibere Tenhorio", false, "Experimentos", 100);
			personagem Sergio = new personagem("Sergio Sacani", false, "Fisica", 100);
			
			System.out.println("Os personagens disponiveis são:");
			System.out.println("Atila Iamarino - Biologo");
			System.out.println("Pirula - Paleontologo");
			System.out.println("Felipe Castanhari - Canal Nostalgia");
			System.out.println("Ibere Thenorio - Canal Manual do mundo");
			System.out.println("Sergio Sacani - Fisica");
			System.out.println("");
			System.out.println("Jogador 1 escolha seu personagem pela inicial do nome:");
			String personagem1 = Scan.nextLine(); 
				switch(personagem1) {
				case "A":
					Atila.ativar(); 
					System.out.println("Você escolheu o Atila Iamarino");
					break;
				case "P":
					Pirula.ativar();
					System.out.println("Você escolheu o Pirula");
					break;
				case "F":
					Castanhari.ativar();
					System.out.println("Você escolheu o Felipe Castanhari");
					break;
				case "I":
					Ibere.ativar();
					System.out.println("Você escolheu o AIbere Thenorio");
					break;
				case "S":
					Sergio.ativar();
					System.out.println("Você escolheu o Sergio Sacani");
					break;
				default:
					System.out.println("Opção Inválida");
					break;
				}
			
			
			
			break;
		case 2:
			System.out.println("Este jogo foi desenvolvido unicamente por Danie Moacir de Ávila."); 
			System.out.println("Aluno do curso de Sistemas de informação na UNA.");
			System.out.println("Quando os outros membros de seu grupo optaram por não realizar o trabalho, Daniel o fez sozinho.");
			System.out.println("O desenvolvedor tem 22 anos, cursa o segundo periodo e escolheu esse curso por seu interesse em games.");
			System.out.println("Tem por objetivo se especializar em desenvolvimento de games.");
			break;
		case 3: 
			System.out.println("O jogo consiste em um duelo de perguntas e respostas entre dois jogadores.");
			System.out.println("Cada jogador escolhe um personagem baseado em youtubers importantes focados em ciência.");
			System.out.println("Os dois começam com 100 pontos de vida e a cada resposta errada é perdido 5 pontos.");
			System.out.println("O jogador que tiver a vida zerada primeiro será considerado derrotado.");
			System.out.println("Qualquer jogador pode decidir interromper o jogo pressionando a letra q (quit).");
			System.out.println("Se os dois estiverem de acordo em interromper o jogo o vencedor é quem tem mais pontos de vida.");
			System.out.println("Se um deles não quiser interromper o jogo ele ganha 15 pontos de vida e quem interrompeu perde 15 pontos.");
			break;
		case 4:
			break;
		default:
			System.out.println("Opção Inválida");
		}
		
		
	}

}

import java.util.Scanner;

public class Jogador {

	public void iniciarJogador() {
		Scanner Scan = new Scanner(System.in);
		
		System.out.println("Seja bem vindo Jogador!");
		System.out.println("Insira a seguir suas informações:");
		System.out.println("Qual o seu nome?");
		String nome = Scan.nextLine(); 
		System.out.println("Qual o seu apelido");
		String apelido = Scan.nextLine(); 
		System.out.println("Qual o seu email?");
		String email = Scan.nextLine(); 
		System.out.println("Qual o seu telefone?");
		String telefone = Scan.nextLine(); 
		
		
	}
}



public class personagem {
	String nome;
	boolean status = false;
	String habilidade;
	int vida = 100;
	
	 public void ativar() {
		 status = true;
	 }
	
	public String getnome() {
        return nome;
	}
	public void setnome(String nome) {
        this.nome = nome;
    }
	
	public boolean getstatus() {
        return status;
	}
	public void setstatus(boolean status) {
        this.status = false;
    }
	
	public String gethabilidade() {
        return habilidade;
	}
	public void sethabilidade(String habilidade) {
        this.habilidade = habilidade;
    }
	
	public int getvida() {
        return vida;
	}
	public void setvida(int vida) {
        this.vida = vida;
    }

	
    public personagem(String nome, boolean status, String habilidade, int vida){ //Metodo cosntrutor
    	this.nome = nome;
    	this.status = status;
    	this.habilidade = habilidade;
    	this.vida = vida;
    }

}


