 def simulasi_tumpukan_file_berkas():
    laci = []

    def push(x):
        laci.append(x)

    def pop():
        return laci.pop()

    for i in range(5):
        x = input("Masukkan file berkas ke laci: ")
        push(x)
        print("Laci saat ini: ", laci)

    print("Mulai mengeluarkan file dari laci (pop):")
    while laci:
        print("Pop file berkas: ", pop())
        print("Laci saat ini: ", laci)

simulasi_tumpukan_file_berkas()                
