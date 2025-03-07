// Judul: Mencari Volume dan Luas Permukaan Silinder
// Memodifikasi dengan Class
// Jumat 7 Maret 2025
// Programmer: Syella Novita Amelia

#include <iostream>
#include <cmath>

using namespace std;

// Kelas untuk merepresentasikan silinder
class Silinder {
private:
    float jariJari;
    float tinggi;

public:
    // Konstruktor untuk inisialisasi nilai saat objek dibuat
    Silinder(float r, float t) {
        jariJari = r;
        tinggi = t;
        cout << "\nObjek silinder berhasil dibuat.\n";
    }

    // Destruktor, dipanggil saat objek keluar dari scope
    ~Silinder() {
        cout << "\nObjek silinder dihapus dari memori.\n";
    }

    // Fungsi untuk menghitung volume silinder
    float hitungVolume() {
        return M_PI * jariJari * jariJari * tinggi;
    }

    // Fungsi untuk menghitung luas permukaan silinder
    float hitungLuasPermukaan() {
        return (2 * M_PI * jariJari * tinggi) + (2 * M_PI * jariJari * jariJari);
    }

    // Menampilkan hasil perhitungan
    void tampilkanHasil() {
        cout << "\n=== Hasil Perhitungan ===\n";
        cout << "Jari-jari        : " << jariJari << endl;
        cout << "Tinggi           : " << tinggi << endl;
        cout << "Volume           : " << hitungVolume() << endl;
        cout << "Luas Permukaan   : " << hitungLuasPermukaan() << endl;
    }
};

// Program utama
int main() {
    float jariJari, tinggi;

    cout << "\n=== Program Menghitung Volume dan Luas Permukaan Silinder ===\n";
    cout << "\nMasukkan jari-jari: ";
    cin >> jariJari;
    cout << "Masukkan tinggi: ";
    cin >> tinggi;

    // Membuat objek silinder
    Silinder silinder(jariJari, tinggi);

    // Menampilkan hasil perhitungan
    silinder.tampilkanHasil();

    cout << "\nTerima kasih telah menggunakan program ini!\n";

    return 0;
}
