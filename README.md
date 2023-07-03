from estrutura_elementar import estrutura_elementar


class No:
    def __init__(self, valor):
        self.valor = valor
        self.proximo = None

    def set_proximo(self, no):
        self.proximo = no

    def get_proximo(self):
        return self.proximo


class LinkedList(estrutura_elementar):
    def __init__(self):
        self.inicio = None

    def inserir_inicio(self, valor):
        if self.inicio is None:
            self.inicio = No(valor)
        else:
            novoNo = No(valor)
            novoNo.set_proximo(self.inicio)
            self.inicio = novoNo

    def inserir_fim(self, valor):
        if self.inicio is None:
            self.inicio = No(valor)
        else:
            novoNo = No(valor)
            aux = self.inicio
            while aux.get_proximo() is not None:
                aux = aux.get_proximo()
            aux.set_proximo(novoNo)

    def esta_vazio(self) -> bool:
       if len(self.valor)==0:
         return True
       else:
        return False

    def remove(self, item):
        if item in self.valor:
            self.valor.remove(item)
            print("item removido com sucesso")  
        else:
            print("o item não existi na lista ")
        pass

    def tamanho(self) -> int:
        if len(self.valor):
          return 1

    def limpa(self):
        self.valor=[]
        pass

    def procura(self, item) -> bool:
        if item in self.valor:
            return True
        else:
          return False

    def indice_de(self, item):
        if item in self.valor:
           return self.valor.index(valor)
        else:
           return 1

    def recupera_indice(self, index):
    
        if 0 <= index <len(self.valor):
            return self.v[index]
        else:
            return 1
