# STM32 Signal Waveform Generator (DAC & DMA)

This project demonstrates how to generate different waveforms (Sine, Cosine, Triangle, Square) using the STM32's built-in DAC (Digital-to-Analog Converter) and DMA (Direct Memory Access) for high-performance, background signal processing.

## Features
- **Waveform Variety:** Supports Sine, Cosine, Triangle, and Square waves.
- **Efficient Processing:** Uses DMA to transfer data from memory to the DAC, minimizing CPU overhead.
- **Timer Triggered:** Precision timing provided by TIM6 to trigger DAC output updates.
- **Interactive:** Change waveform types dynamically using the onboard push-button (EXTI).
- **Configurable:** Adjustable amplitude and frequency functions included.

## Technical Details
- **Microcontroller:** STM32 (Targeting ARM-based architecture)
- **Peripheral Usage:** DAC, DMA, TIM6, GPIO (EXTI)
- **Language:** C (HAL Library)

## How It Works
1. **Waveform Buffers:** Pre-calculated arrays (`sine_val`, `cos_val`, etc.) are stored in memory.
2. **DMA Transfer:** The DAC is configured to be triggered by TIM6 update events, and DMA continuously feeds data to the DAC register.
3. **Interrupts:** User button (PC13) utilizes external interrupts to toggle between waveform types.

## License
Copyright (c) 2026 STMicroelectronics. This project is provided as-is under the terms found in the LICENSE file.



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



# STM32 Sinyal Dalga Formu Üreteci (DAC & DMA)

Bu proje, STM32'nin yerleşik DAC (Dijital-Analog Dönüştürücü) ve DMA (Doğrudan Bellek Erişimi) özelliklerini kullanarak farklı dalga formları (Sinüs, Kosinüs, Üçgen, Kare) üretmeyi gösteren bir uygulamadır.

## Özellikler
- **Dalga Çeşitliliği:** Sinüs, Kosinüs, Üçgen ve Kare dalga destekleri.
- **Verimli İşlem:** DMA kullanılarak verilerin bellekten DAC'a doğrudan aktarılması, CPU yükünü minimize eder.
- **Zamanlayıcı Tetikleme:** DAC çıkış güncellemeleri TIM6 zamanlayıcısı ile hassas bir şekilde kontrol edilir.
- **Etkileşimli:** Dahili buton (EXTI) kullanılarak dalga tipleri dinamik olarak değiştirilebilir.
- **Yapılandırılabilir:** Genlik (Amplitude) ve frekans ayarları yapılabilir fonksiyonlara sahiptir.

## Teknik Detaylar
- **Mikrokontrolcü:** STM32 (ARM tabanlı mimari)
- **Kullanılan Çevre Birimleri:** DAC, DMA, TIM6, GPIO (EXTI)
- **Programlama Dili:** C (HAL Kütüphanesi)

## Çalışma Mantığı
1. **Dalga Tamponları:** Önceden hesaplanmış diziler (`sine_val`, `cos_val` vb.) bellekte tutulur.
2. **DMA Aktarımı:** DAC, TIM6 güncelleme olaylarıyla tetiklenecek şekilde yapılandırılmıştır ve DMA, verileri sürekli olarak DAC kaydedicisine iletir.
3. **Kesmeler:** Kullanıcı butonu (PC13), harici kesmeler (interrupt) kullanılarak dalga tipleri arasında geçiş yapılmasını sağlar.

## Lisans
Telif Hakkı (c) 2026 STMicroelectronics. Bu proje, LICENSE dosyasında belirtilen koşullar altında "olduğu gibi" sağlanmıştır.
