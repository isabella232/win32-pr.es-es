---
description: Con el aumento de los dispositivos de almacenamiento multimedia que requieren formatos de audio comprimidos, las aplicaciones deben identificar, describir y usar una variedad de contenido de audio codificado nuevo para transmitir contenido desde equipos a dispositivos como el receptor HDMI o DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Representación de formatos para transmisiones IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a607770a388a11978d0e4666b5046506b6698c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549300"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Representación de formatos para transmisiones IEC 61937

Con el aumento de los dispositivos de almacenamiento multimedia que requieren formatos de audio comprimidos, las aplicaciones deben identificar, describir y usar una variedad de contenido de audio codificado nuevo para transmitir contenido desde equipos a dispositivos como el receptor HDMI o DisplayPort.

Para representar una secuencia de audio codificada que se transmitirá a través de una interfaz compatible con IEC 61937, una aplicación debe proporcionar:

-   Características de una secuencia de audio codificada que se va a transmitir.

-   Características de una secuencia de audio descodificada en el dispositivo de destino.

En Windows Vista y sistemas operativos Windows anteriores, una aplicación puede deducir el nivel de calidad de un formato de audio a partir del número de canales, el tamaño de la muestra y la velocidad de datos de una secuencia de audio que usa el formato. En el caso de un formato PCM, esta información está disponible en los miembros **nChannels**, **nSamplesPerSec** y **nAvgBytesPerSec** de la **estructuraSAMPLEATEX** que especifica el formato. En el caso de un formato que no es PCM, se ha comandos a estos tres miembros para almacenar información sobre los datos comprimidos en la secuencia de audio. Por lo tanto, la estructura **DESATEX** carece de información sobre el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de la secuencia de audio que no es PCM después de que la secuencia se descomprima y se reproduce. En función de la información de esta estructura, es posible que un usuario o una aplicación tengan dificultades para deducir el nivel de calidad de la secuencia que no es de PCM.

**EL ELEMENTO DESATEX** se ha ampliado a la **estructura DESATEXTENSIBLE** para proporcionar las características de flujo adicionales. Sin embargo, esta estructura tampoco es adecuada para describir la secuencia para las transmisiones IEC 61937 porque estaba diseñada para representar un único conjunto de características y se usaba para datos PCM de varios canales sin comprimir.

En Windows 7, el sistema operativo soluciona este problema al proporcionar compatibilidad con una nueva estructura, **SOAPATEXTENSIBLE \_ IEC61937,** que extiende la estructura **DESATEXTENSIBLE** para almacenar dos conjuntos de características de secuencia de audio: el formato de audio codificado antes de la transmisión y las características de la secuencia de audio después de que se haya descodificado. La nueva estructura especifica explícitamente el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de un formato que no es PCM. Con esta información, una aplicación puede deducir el nivel de calidad de la secuencia que no es PCM después de descomprimida y reproducida.

La **estructura DELATEXTENSIBLE \_ IEC61937** se declara en el encabezado KsMedia.h incluido con el SDK de Windows 7. El **miembro FormatExt** es la estructura **WAVEFORMATEXTENSIBLE** que almacena las características de la secuencia que se va a transmitir. El **miembro Format** de la estructura **WAVEFORMATEXTENSIBLE** es la estructura DE **FORMADEDATOSTEX.** El contenido de **esta estructura DESATEX** y **DESATEXTENSIBLE** indica a una aplicación si la estructura se puede interpretar como una estructura **DE FORMAENSIBLE \_ IEC61937.** Para una **estructura DE FORMAENTEXTENSIBLE \_ IEC61937:**

-   El **miembro wFormatTag** de **WAVEATEX** debe contener WAVE \_ FORMAT EXTENSIBLE ( \_ `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   El **miembro SubFormat** de la **estructura SOAPATEXTENSIBLE** especifica el GUID del formato codificado que se va a transmitir. Por ejemplo, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica el formato Dolby Digital Plus. Para ver los GUID admitidos, consulte GUID de subformato.

-   El tamaño indicado por el **miembro cbSize** de LA FORMADETEX es de 34 bytes. (`FormatExt.Format.cbSize = 34`). El tamaño total de **WAVEFORMATEXTENSIBLE \_ IEC61937** es de 52 bytes.

Los miembros **dwEncodedSamplesPerSec,** **dwEncodedChannelCount** y **dwAverageBytesPerSec** **deSAMPLEATEXTENSIBLE \_ IEC61937** describen la frecuencia de muestreo, el número de canales y la velocidad de bits en bytes de la secuencia de audio después de que se haya descodificado.

## <a name="subformat-guids"></a>GUID de subformato

En Windows 7, el encabezado KsMedia.h contiene definiciones para los GUID de subformato para los formatos de audio comprimidos definidos por CEA-861-D. Los GUID se especifican en el miembro SubFormat del **objeto DEFORMATEXTENSIBLE**, especificado en el **miembro FormatExt** de la estructura **DEILATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Los GUID para los formatos de audio comprimidos que están disponibles como formatos de audio codificados iec 61937 estándar se enumeran en la tabla siguiente. Estos formatos son similares a los formatos active coding 3 (AC-3) y digital sound (DTS) existentes en Windows.



| Tipo CEA 861 | GUID de subformato                                                                                                          | Descripción                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Consulte la secuencia.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> SUBTIPO DE SUBTIPO \_ \_ KSDATAFORMATOTEX<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL<br/>              | AC-3                                         |
| 0x03         | 00000003-0bio-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (Nivel 1 & 2)                         |
| 0x04         | 00000004-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (capa 3)                             |
| 0x05         | 00000005-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (multicanal)                         |
| 0x06         | 00000006-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ AAC<br/>                         | Codificación de audio avanzada (MPEG-2/4 AAC en ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0a         | 0000000a-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL \_ PLUS<br/>        | Dolby Digital Plus                           |
| 0x0a         | 0000010a-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY DIGITAL PLUS \_ \_ \_ ATMOS<br/> | Dolby Atmos codificado con Dolby Digital Plus  |
| 0x0b         | 0000000b-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS \_ HD<br/> | DTS HD  |
| 0x0b         | 0000010b-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTSX \_ E1<br/> | DTS:X E1  |
| 0x0b         | 0000030b-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTSX \_ E2<br/> | DTS:X E2  |
| 0x0f         |                                                                                                                         | Reservado sin usar                              |



 

Los GUID para los formatos de audio comprimidos que se transmiten en paquetes de ejemplo de audio de alta velocidad de bits se enumeran en la tabla siguiente.



| Tipo CEA 861 | GUID de subformato                                                                                           | Descripción                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0b         | 0000000b-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 bits, 96 Khz)                                                                                                          |
| 0x0c         | 0000000c-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MLP<br/>   | Dolby MAT 1.0:<br/> Dolby TrueHD (MLP – Empaquetado sin pérdida de meridiano): 24 bits a 192 KHz/hasta 18 Mbps, 8 canales) <br/> |
| 0x0c         | 0000010c-0junto-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MAT20<br/> | Dolby MAT 2.0: <br/> Dolby TrueHD: 24 bits a 192 KHz/hasta 18 Mbps, 8 canales o LPCM de hasta 24 Mbps. <br/>           |
| 0x0c         | 0000030c-0junto-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MAT21<br/> | Dolby MAT 2.1: <br/> Dolby TrueHD: 24 bits a 192 KHz/hasta 18 Mbps, 8 canales o LPCM de hasta 24 Mbps. <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ WMA \_ PRO<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

El controlador de la clase HD Audio proporcionado por Microsoft admite los formatos PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP). Los GUID para los formatos de audio comprimidos que no son compatibles con el controlador de la clase de audio HD y que se pueden implementar mediante soluciones de terceros se enumeran en la tabla siguiente.



| Tipo CEA 861 | GUID de subformato                                                                                              | Descripción                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ ATRAC<br/>           | Codificación acústica de transformación adaptable (ATRAC)                                     |
| 0x09         | 00000009-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ AUDIO DE UN \_ \_ BIT<br/> | One-Bit Audio                                                                  |
| 0x0d         | 0000000d-0ciso-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DST<br/>             | Transporte de flujo directo (DST): DSD comprimido sin pérdida (Direct Stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Formato Dolby Digital Plus

Cuando el contenido de Dolby Digital Plus se transmite a través de IEC 60958, la velocidad de muestreo del vínculo debe ser cuatro veces la frecuencia de muestreo del contenido. Dolby Digital Plus admite velocidades de muestreo de contenido de 32 KHz, 44,1 KHz y 48 KHz. Las interfaces como HDMI no admiten frecuencias de muestreo de contenido de 128 KHz (32 KHz x 4), por lo que solo se pueden admitir frecuencias de muestreo de contenido de 44,1 y 48 KHz.

En el ejemplo siguiente se muestran los valores establecidos por una aplicación en la estructura DESATEXTENSIBLE IEC61937 para representar el formato Dolby Digital Plus a una velocidad de muestreo de contenido de \_ 48 KHz.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (MAT)

El contenido Dolby TrueHD se transmite a través de IEC 60958 a 176,4 kHz/8 canales (lo que requiere una velocidad de fotogramas IEC 60958 de 705,6 kHz) para las velocidades de muestra de contenido de 44,1, 88,2 y 176,4 kHz y 192 kHz/8 canales (que requieren una velocidad de fotogramas IEC 60958 de 768 kHz) para velocidades de muestreo de contenido de 48, 96 y 192 kHz.

En los ejemplos siguientes se muestran los valores establecidos por una aplicación en la estructura DESATEXTENSIBLE IEC61937 para representar Dolby TrueHD a una velocidad de muestra de contenido de \_ 96 KHz.

Dolby MAT 1.0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2.0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2.1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> La compatibilidad con una versión de Dolby MAT no implica compatibilidad con Dolby MAT con un número de versión inferior. Dado que Dolby MAT 2.1 es compatible con versiones anteriores de Dolby MAT, un controlador de clase que indica la compatibilidad con Dolby MAT 2.1 normalmente también indicará la compatibilidad con Dolby MAT 2.0 y Dolby MAT 1.0, mediante una estructura SEPARATEATEXTENSIBLE IEC61937 independiente para cada \_ versión.

 

## <a name="wma-pro"></a>WMA Pro

El contenido de audio de WMA Pro se puede codificar en uno de los cuatro perfiles enumerados en la tabla siguiente.



| Perfil | Propiedad: valor                                                                                                                                                                                                                                                      | Descripción                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Velocidad de bits máxima: 192 000 bps <br/> Frecuencia de muestreo máxima: 48 KHz <br/> Número máximo de canales: 2 <br/> Tamaño máximo del búfer: 600 \* 1024 bits <br/> Máximo de muestras por fotograma: 2048 <br/> Bits máximos por fotograma: 655536<br/>   | Se recomienda para música y streaming por vía aérea.<br/> La velocidad máxima de bits en un fotograma de audio es de 1536 000 bps.<br/>          |
| M1      | Velocidad de bits máxima: 385 000 bps <br/> Frecuencia de muestreo máxima: 48 KHz <br/> Número máximo de canales: 6 <br/> Tamaño máximo del búfer: 600 \* 1024 bits <br/> Máximo de muestras por fotograma: 4096 <br/> Bits máximos por fotograma: 131072<br/>   | Se recomienda para películas de definición estándar de sonido envolvente.<br/> La velocidad máxima de bits en un fotograma de audio es de 1536 000 bps.<br/> |
| M2      | Velocidad de bits máxima: 769000 bps <br/> Frecuencia de muestreo máxima: 96 KHz <br/> Número máximo de canales: 6 <br/> Tamaño máximo del búfer: 1200 \* 1024 bits <br/> Máximo de muestras por fotograma: 4096 <br/> Bits máximos por fotograma: 131072<br/>  | Se recomienda para películas de alta definición de sonido envolvente.<br/> La velocidad máxima en un fotograma de audio es 3072000 bps.<br/>         |
| M3      | Velocidad de bits máxima: 300 0000 bps <br/> Frecuencia de muestreo máxima: 96 KHz <br/> Número máximo de canales: 8 <br/> Tamaño máximo del búfer: 2400 \* 1024 bits <br/> Máximo de muestras por fotograma: 4096 <br/> Bits máximos por fotograma: 131072<br/> | Recomendado para el cine digital.<br/> La velocidad máxima en un fotograma de audio es 3072000 bps.<br/>                               |



 

Los perfiles M0 y M1 caben en una secuencia IEC 60958 de 48 KHz/16 bits/estéreo (1536000 bps). Los perfiles M2 y M3 caben en una secuencia IEC 60958 de 96 KHz/16 bits/estéreo (3072000 bps).

En el ejemplo siguiente se muestran los valores establecidos por una aplicación en la estructura DESATEXTENSIBLE IEC61937 para representar WMA Pro como \_ un perfil M2.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de dispositivo](device-formats.md)
</dt> </dl>

 

 




