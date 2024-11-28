# Exercise 6: Eliminating Resource Contention by Suspending the Scheduler

## Tujuan
1. Menunjukkan cara menghilangkan kontensi sumber daya dengan menghentikan sementara penjadwalan (suspending scheduler).
2. Memahami pengaruh fungsi vTaskSuspendAll() dan xTaskResumeAll() dalam sistem multitasking.

## Peralatan

1. STM32F103C8T
2. LED
3. Kabel Jummper
4. Mini debugger
 

## Langkah Implementasi

##### Persiapan Proyek

1. Aktifkan FreeRTOS melalui STM32CubeMX.
2. Tambahkan dua tugas (Task1 dan Task2) yang mencoba mengakses sumber daya bersama. Implementasi Kode
2. Modifikasi kode untuk menambahkan fungsi vTaskSuspendAll() sebelum akses ke sumber daya bersama dan xTaskResumeAll() setelahnya.
3. Gunakan osDelay() untuk mensimulasikan tugas yang berjalan secara periodik. Uji Program
4. Flash program ke board.
5. Amati perbedaan perilaku sistem sebelum dan sesudah menggunakan fungsi suspend/resume scheduler.


## Hasil yang Diharapkan
1. Tanpa Suspend Scheduler: Terjadi konflik dalam akses sumber daya bersama.
2. Dengan Suspend Scheduler: Konflik dapat dihindari karena hanya satu tugas yang dapat mengakses sumber daya dalam satu waktu

## Hasil Percobaan
https://github.com/user-attachments/assets/c421cb40-0249-4539-9892-b5598f8bc1dc
