# pythonProjectUniceub
Python Programming Logic Credit Project

# Classe 1 – Vacinação Covid
class VacinacaoCovid:
    def __init__(self):
        self.Laboratorio = ""
        self.Doses = 0

    def setLaboratorio(self, Laboratorio):
        self.Laboratorio = Laboratorio

    def getLaboratorio(self):
        return self.Laboratorio

    def setDoses(self, Doses):
        self.Doses = Doses

    def getDoses(self):
        return self.Doses


# Classe 2 - Brasília
class Brasilia(VacinacaoCovid):
    def __init__(self):
        super().__init__()

    def main(self):
        # Aplicação de herança utilizando os atributos da Classe superior
        brasilia1 = Brasilia()
        brasilia1.setLaboratorio("oxford")
        brasilia1.setDoses(2)

        # Aplicação de herança utilizando o objeto da Classe superior
        vacinacaocovid1 = VacinacaoCovid()
        vacinacaocovid1.setLaboratorio("jansen")
        vacinacaocovid1.setDoses(1)

        print("Laboratorio:", brasilia1.getLaboratorio())
        print("Doses:", brasilia1.getDoses())

        print("Laboratorio:", vacinacaocovid1.getLaboratorio())
        print("Doses:", vacinacaocovid1.getDoses())


# Polimorfismo
class Influenza(VacinacaoCovid):
    def __init__(self):
        super().__init__()

    def main(self):
        influenza1 = Influenza()
        influenza1.setLaboratorio("GSK")
        influenza1.setDoses(1)

        print("Laboratorio:", influenza1.getLaboratorio())
        print("Doses:", influenza1.getDoses())


# Testando as classes
if __name__ == "__main__":
    # Testando a classe Brasilia
    brasilia_instance = Brasilia()
    brasilia_instance.main()

    # Testando a classe Influenza
    influenza_instance = Influenza()
    influenza_instance.main()

