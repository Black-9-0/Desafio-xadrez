desafio_xadrez.

class Peca: def init(self, cor): self.cor = cor

def movimentos_possiveis(self, posicao, tabuleiro):
    return []

class Rei(Peca): def str(self): return 'R' if self.cor == 'branco' else 'r'

class Rainha(Peca): def str(self): return 'Q' if self.cor == 'branco' else 'q'

class Torre(Peca): def str(self): return 'T' if self.cor == 'branco' else 't'

class Bispo(Peca): def str(self): return 'B' if self.cor == 'branco' else 'b'

class Cavalo(Peca): def str(self): return 'C' if self.cor == 'branco' else 'c'

class Peao(Peca): def str(self): return 'P' if self.cor == 'branco' else 'p'

class Tabuleiro: def init(self): self.tabuleiro = self.criar_tabuleiro_inicial()

def criar_tabuleiro_inicial(self):
    t = [[None for _ in range(8)] for _ in range(8)]
    cores = ['branco', 'preto']

    # Peças brancas
    t[0] = [Torre('branco'), Cavalo('branco'), Bispo('branco'), Rainha('branco'),
           Rei('branco'), Bispo('branco'), Cavalo('branco'), Torre('branco')]
    t[1] = [Peao('branco') for _ in range(8)]

    # Peças pretas
    t[6] = [Peao('preto') for _ in range(8)]
    t[7] = [Torre('preto'), Cavalo('preto'), Bispo('preto'), Rainha('preto'),
           Rei('preto'), Bispo('preto'), Cavalo('preto'), Torre('
