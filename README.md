# Program1
# bahasa pemrograman pertemuan ke-13
**Codingan**

```
import tkinter as tk
from view.input_form import InputForm
from view.mahasiswa import MahasiswaView
from data.mahasiswa import DataMahasiswa

class MainApp:
    def __init__(self, master):
        self.master = master
        self.master.title("Aplikasi Data Mahasiswa")

        self.data_mahasiswa = DataMahasiswa()

        self._create_widgets()

    def _create_widgets(self):
        self.button_input = tk.Button(self.master, text="Input Mahasiswa", command=self.open_input_form)
        self.button_input.pack(pady=10)

        self.button_view = tk.Button(self.master, text="Lihat Daftar Mahasiswa", command=self.open_mahasiswa_view)
        self.button_view.pack(pady=10)

    def open_input_form(self):
        self._open_new_window(InputForm)

    def open_mahasiswa_view(self):
        self._open_new_window(MahasiswaView)

    def _open_new_window(self, view_class):
        new_window = tk.Toplevel(self.master)
        view_class(new_window, self.data_mahasiswa)

if __name__ == "__main__":
    root = tk.Tk()
    app = MainApp(root)
    root.mainloop()
```


# Hasil
**Awal Mula**
![Cuplikan layar 2024-12-09 142056(2)](https://github.com/user-attachments/assets/df156b46-4adb-4a95-ad15-9e0b6152dfd4)


**Setelah menginput Nama, NIM, dan Jurusan**
![Cuplikan layar 2024-12-09 142056](https://github.com/user-attachments/assets/69dd4098-3e8c-4ccf-aa53-f4dca987701d)


**Setelah mengubah Hasil**
![Cuplikan layar 2024-12-09 142131](https://github.com/user-attachments/assets/46895839-4bfc-4dfc-8bde-9885171a5f21)


**Setelah dihapus salah satu hasil**
![Cuplikan layar 2024-12-09 142145](https://github.com/user-attachments/assets/4883da50-1554-4e65-b509-9f7f0b4be0a4)


**SELESAI**
