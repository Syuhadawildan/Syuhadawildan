   
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


class LinkedList:
    def __init__(self):
        self.head = None

    def insert_at_end(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            return

        temp = self.head
        while temp.next is not None:
            temp = temp.next

        temp.next = new_node

    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def insert_after(self, prev_node, data):
        if prev_node is None:
            print("Node sebelumnya yang diberikan tidak boleh kosong")
            return

        new_node = Node(data)
        new_node.next = prev_node.next
        prev_node.next = new_node

    def search(self, key):
        temp = self.head
        while temp is not None:
            if temp.data == key:
                return temp
            temp = temp.next
        return None

    def delete_at_beginning(self):
        if self.head is None:
            return None

        temp = self.head
        self.head = self.head.next
        return temp.data

    def delete_at_end(self):
        if self.head is None:
            return None

        temp = self.head
        if temp.next is None:
            self.head = None
            return temp.data

        while temp.next.next is not None:
            temp = temp.next

        deleted_data = temp.next.data
        temp.next = None
        return deleted_data

    def print_list(self):
        temp = self.head
        while temp is not None:
            print(temp.data, end=" ")
            temp = temp.next
        print()


linked_list = LinkedList()
linked_list.insert_at_end(10)
linked_list.insert_at_end(20)
linked_list.insert_at_end(30)
linked_list.insert_at_beginning(5)
linked_list.insert_after(linked_list.head.next, 15)

print("Linked list:")
linked_list.print_list()

print("\nMencari node dengan nilai 15:")
found_node = linked_list.search(15)
if found_node:
    print("Node ditemukan:", found_node.data)
else:
    print("Node tidak ditemukan")

print("\nMenghapus node pertama:")
deleted_data = linked_list.delete_at_beginning()
print("Data yang dihapus:", deleted_data)
linked_list.print_list()

print("\nMenghapus node terakhir:")
deleted_data = linked_list.delete_at_end()
print("Data yang dihapus:


𝘤𝘭𝘢𝘴𝘴 𝘕𝘰𝘥𝘦:
    𝘥𝘦𝘧 __𝘪𝘯𝘪𝘵__(𝘴𝘦𝘭𝘧, 𝘬𝘦𝘺):
        𝘴𝘦𝘭𝘧.𝘬𝘦𝘺 = 𝘬𝘦𝘺
        𝘴𝘦𝘭𝘧.𝘭𝘦𝘧𝘵 = 𝘕𝘰𝘯𝘦
        𝘴𝘦𝘭𝘧.𝘳𝘪𝘨𝘩𝘵 = 𝘕𝘰𝘯𝘦


    𝘥𝘦𝘧 𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 𝘬𝘦𝘺):
        𝘪𝘧 𝘳𝘰𝘰𝘵 𝘪𝘴 𝘕𝘰𝘯𝘦:
            𝘳𝘦𝘵𝘶𝘳𝘯 𝘕𝘰𝘥𝘦(𝘬𝘦𝘺)
        𝘦𝘭𝘪𝘧 𝘬𝘦𝘺 < 𝘳𝘰𝘰𝘵.𝘬𝘦𝘺:
            𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵, 𝘬𝘦𝘺)
        𝘦𝘭𝘴𝘦:
            𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵, 𝘬𝘦𝘺)
        𝘳𝘦𝘵𝘶𝘳𝘯 𝘳𝘰𝘰𝘵


    𝘥𝘦𝘧 𝘴𝘦𝘢𝘳𝘤𝘩(𝘳𝘰𝘰𝘵, 𝘬𝘦𝘺):
        𝘪𝘧 𝘳𝘰𝘰𝘵 𝘪𝘴 𝘕𝘰𝘯𝘦:
            𝘳𝘦𝘵𝘶𝘳𝘯 𝘍𝘢𝘭𝘴𝘦
        𝘦𝘭𝘪𝘧 𝘬𝘦𝘺 < 𝘳𝘰𝘰𝘵.𝘬𝘦𝘺:
            𝘳𝘦𝘵𝘶𝘳𝘯 𝘕𝘰𝘥𝘦.𝘴𝘦𝘢𝘳𝘤𝘩(𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵, 𝘬𝘦𝘺)
        𝘦𝘭𝘪𝘧 𝘬𝘦𝘺 > 𝘳𝘰𝘰𝘵.𝘬𝘦𝘺:
            𝘳𝘦𝘵𝘶𝘳𝘯 𝘕𝘰𝘥𝘦.𝘴𝘦𝘢𝘳𝘤𝘩(𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵, 𝘬𝘦𝘺)
        𝘦𝘭𝘴𝘦:
            𝘳𝘦𝘵𝘶𝘳𝘯 𝘛𝘳𝘶𝘦


    𝘥𝘦𝘧 𝘱𝘳𝘦𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵):
        𝘪𝘧 𝘳𝘰𝘰𝘵 𝘪𝘴 𝘯𝘰𝘵 𝘕𝘰𝘯𝘦:
            𝘱𝘳𝘪𝘯𝘵(𝘳𝘰𝘰𝘵.𝘬𝘦𝘺)
            𝘕𝘰𝘥𝘦.𝘱𝘳𝘦𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵)
            𝘕𝘰𝘥𝘦.𝘱𝘳𝘦𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵)


    𝘥𝘦𝘧 𝘪𝘯𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵):
        𝘪𝘧 𝘳𝘰𝘰𝘵 𝘪𝘴 𝘯𝘰𝘵 𝘕𝘰𝘯𝘦:
            𝘕𝘰𝘥𝘦.𝘪𝘯𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵)
            𝘱𝘳𝘪𝘯𝘵(𝘳𝘰𝘰𝘵.𝘬𝘦𝘺)
            𝘕𝘰𝘥𝘦.𝘪𝘯𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵)

  
    𝘥𝘦𝘧 𝘱𝘰𝘴𝘵𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵):
        𝘪𝘧 𝘳𝘰𝘰𝘵 𝘪𝘴 𝘯𝘰𝘵 𝘕𝘰𝘯𝘦:
            𝘕𝘰𝘥𝘦.𝘱𝘰𝘴𝘵𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘭𝘦𝘧𝘵)
            𝘕𝘰𝘥𝘦.𝘱𝘰𝘴𝘵𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵.𝘳𝘪𝘨𝘩𝘵)
            𝘱𝘳𝘪𝘯𝘵(𝘳𝘰𝘰𝘵.𝘬𝘦𝘺)


𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘯𝘦
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 10)
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 5)
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 15)
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 3)
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 12)
𝘳𝘰𝘰𝘵 = 𝘕𝘰𝘥𝘦.𝘪𝘯𝘴𝘦𝘳𝘵(𝘳𝘰𝘰𝘵, 20)

𝘪𝘧 𝘕𝘰𝘥𝘦.𝘴𝘦𝘢𝘳𝘤𝘩(𝘳𝘰𝘰𝘵, 15):
    𝘱𝘳𝘪𝘯𝘵("𝘕𝘪𝘭𝘢𝘪 15 𝘥𝘪𝘵𝘦𝘮𝘶𝘬𝘢𝘯 𝘥𝘢𝘭𝘢𝘮 𝘱𝘰𝘩𝘰𝘯")
𝘦𝘭𝘴𝘦:
    𝘱𝘳𝘪𝘯𝘵("𝘕𝘪𝘭𝘢𝘪 15 𝘵𝘪𝘥𝘢𝘬 𝘥𝘪𝘵𝘦𝘮𝘶𝘬𝘢𝘯 𝘥𝘢𝘭𝘢𝘮 𝘱𝘰𝘩𝘰𝘯")

𝘱𝘳𝘪𝘯𝘵("𝘗𝘳𝘦𝘰𝘳𝘥𝘦𝘳 𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭:")
𝘕𝘰𝘥𝘦.𝘱𝘳𝘦𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵)

𝘱𝘳𝘪𝘯𝘵("𝘐𝘯𝘰𝘳𝘥𝘦𝘳 𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭:")
𝘕𝘰𝘥𝘦.𝘪𝘯𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵)

𝘱𝘳𝘪𝘯𝘵("𝘗𝘰𝘴𝘵𝘰𝘳𝘥𝘦𝘳 𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭:")
𝘕𝘰𝘥𝘦.𝘱𝘰𝘴𝘵𝘰𝘳𝘥𝘦𝘳_𝘵𝘳𝘢𝘷𝘦𝘳𝘴𝘢𝘭(𝘳𝘰𝘰𝘵)     


def __init__(self, kode, nama, harga, kategori):
        self.kode = kode
        self.nama = nama
        self.harga = harga
        self.kategori = kategori

def main():
    
    produk = {}
   
    produk["P001"] = Produk("P001", "Laptop", 5000000, "Elektronik")
    produk["P002"] = Produk("P002", "Smartphone", 3000000, "Elektronik")
    produk["P003"] = Produk("P003", "Sepatu", 200000, "Pakaian")

   
    kode_produk = input("Masukkan kode produk: ")
    if kode_produk in produk:
        produk_ditemukan = produk[kode_produk]
        print(f"Produk dengan kode {kode_produk}:")
        print(f"- Nama: {produk_ditemukan.nama}")
        print(f"- Harga: {produk_ditemukan.harga}")
        print(f"- Kategori: {produk_ditemukan.kategori}")
    else:
        print(f"Produk dengan kode {kode_produk} tidak ditemukan")

   
    nama_produk = input("Masukkan nama produk: ")
    produk_yang_cocok = []
    for produk_value in produk.values():
        if nama_produk.lower() in produk_value.nama.lower():
            produk_yang_cocok.append(produk_value)
    if produk_yang_cocok:
        print(f"Produk dengan nama yang mengandung '{nama_produk}':")
        for produk in produk_yang_cocok:
            print(f"- {produk.nama}")
    else:
        print(f"Produk dengan nama yang mengandung '{nama_produk}' tidak ditemukan")

    
    kategori = input("Masukkan kategori: ")
    produk_dalam_kategori = []
    for produk_value in produk.values():
        if kategori.lower() == produk_value.kategori.lower():
            produk_dalam_kategori.append(produk_value)
    if produk_dalam_kategori:
        print(f"Produk dalam kategori '{kategori}':")
        for produk in produk_dalam_kategori:
            print(f"- {produk.nama}")
    else:
        print(f"Produk dalam kategori '{kategori}' tidak ditemukan")

if __name__ == "__main__":
    main()     
