---
description: Con el aumento de los dispositivos de almacenamiento de medios que requieren formatos de audio comprimidos, las aplicaciones deben identificar, describir y usar una variedad de contenido de audio codificado nuevo para transmitir contenido desde equipos a dispositivos como HDMI o el receptor de DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Representación de formatos para transmisiones IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659611"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Representación de formatos para transmisiones IEC 61937

Con el aumento de los dispositivos de almacenamiento de medios que requieren formatos de audio comprimidos, las aplicaciones deben identificar, describir y usar una variedad de contenido de audio codificado nuevo para transmitir contenido desde equipos a dispositivos como HDMI o el receptor de DisplayPort.

Para representar una secuencia de audio codificada que se va a transmitir a través de una interfaz compatible con IEC 61937, una aplicación debe proporcionar:

-   Características de una secuencia de audio codificada que se va a transmitir.

-   Características de una secuencia de audio descodificada en el dispositivo de destino.

En Windows Vista y versiones anteriores del sistema operativo Windows, una aplicación puede deducir el nivel de calidad de un formato de audio desde el número de canales, el tamaño de la muestra y la velocidad de datos de una secuencia de audio que utiliza el formato. Para un formato PCM, esta información está disponible en los miembros **nChannels**, **nSamplesPerSec** y **nAvgBytesPerSec** de la estructura **WAVEFORMATEX** que especifica el formato. En el caso de un formato que no sea PCM, estos tres miembros se commandeered para almacenar información sobre los datos comprimidos en la secuencia de audio. Por lo tanto, la estructura **WAVEFORMATEX** no tiene información sobre el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de la secuencia de audio que no es PCM después de descomprimir y reproducir el flujo. En función de la información de esta estructura, un usuario o una aplicación pueden tener dificultades para deducir el nivel de calidad de la secuencia que no es PCM.

El **WAVEFORMATEX** se amplió a la estructura **WAVEFORMATEXTENSIBLE** para proporcionar las características de la secuencia adicional. Sin embargo, esta estructura tampoco es adecuada para describir el flujo para las transmisiones IEC 61937 porque estaba diseñado para representar un único conjunto de características y se utiliza para datos PCM sin comprimir y multicanal.

En Windows 7, el sistema operativo resuelve este problema proporcionando compatibilidad con una nueva estructura, **WAVEFORMATEXTENSIBLE \_ IEC61937** , que extiende la estructura **WAVEFORMATEXTENSIBLE** para almacenar dos conjuntos de características de secuencias de audio: el formato de audio codificado antes de la transmisión y las características de la secuencia de audio una vez descodificada. La nueva estructura especifica explícitamente el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de un formato no PCM. Con esta información, una aplicación puede inferir el nivel de calidad de la secuencia que no es PCM una vez descomprimido y reproducido.

La estructura **WAVEFORMATEXTENSIBLE \_ IEC61937** se declara en el encabezado KsMedia. h incluido en el SDK de Windows 7. El miembro **FormatExt** es la estructura **WAVEFORMATEXTENSIBLE** que almacena las características de la secuencia que se va a transmitir. El miembro **Format** de la estructura **WAVEFORMATEXTENSIBLE** es la estructura **WAVEFORMATEX** . El contenido de este **WAVEFORMATEX** y **WAVEFORMATEXTENSIBLE** indica a una aplicación si la estructura se puede interpretar como una **estructura \_ IEC61937 de WAVEFORMATEXTENSIBLE** . Para una estructura **WAVEFORMATEXTENSIBLE \_ IEC61937** :

-   El miembro **wFormatTag** de **WAVEFORMATEX** debe contener el \_ formato de onda \_ extensible ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   El miembro **subformat** de la estructura **WAVEFORMATEXTENSIBLE** especifica el GUID del formato codificado que se va a transmitir. Por ejemplo, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica el formato Dolby Digital Plus. Para los GUID admitidos, vea subformato de GUID.

-   El tamaño indicado por el miembro **cbSize** de WAVEFORMATEX es de 34 bytes. (`FormatExt.Format.cbSize = 34`). El tamaño total de **WAVEFORMATEXTENSIBLE \_ IEC61937** es de 52 bytes.

Los miembros **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** y **dwAverageBytesPerSec** de **WAVEFORMATEXTENSIBLE \_ IEC61937** describen la velocidad de muestreo, el número de canales y la velocidad de bits en bytes del flujo de la secuencia de audio después de que se haya descodificado.

## <a name="subformat-guids"></a>GUID de subformato

En Windows 7, el encabezado KsMedia. h contiene definiciones de los GUID de subformato para los formatos de audio comprimidos definidos por CEA-861-D. Los GUID se especifican en el miembro subformat de **WAVEFORMATEXTENSIBLE**, especificado en el miembro **FormatExt** de la estructura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

En la tabla siguiente se enumeran los GUID de los formatos de audio comprimidos que están disponibles como formatos de audio codificados estándar IEC 61937. Estos formatos son similares a las representaciones de formatos de código activo 3 (AC-3) y sonido Digital Theater (DTS) existentes en Windows.



| CEA tipo 861 | GUID de subformato                                                                                                          | Descripción                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Haga referencia a la secuencia.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ WAVEFORMATEX<br/>                          | PCM IEC 60958                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (capa 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (capa 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (multicanal)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ AAC<br/>                         | Codificación de audio avanzada (MPEG-2/4 AAC en ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| STOP         | 0000000a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus<br/>        | Dolby Digital Plus                           |
| STOP         | 0000010a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus \_ Atmos<br/> | Dolby Digital Plus codificado  |
| 0x0f         |                                                                                                                         | Reservado sin usar                              |



 

Los GUID de los formatos de audio comprimidos que se transmiten en paquetes de ejemplo de audio de alta velocidad de bits se muestran en la tabla siguiente.



| CEA tipo 861 | GUID de subformato                                                                                           | Descripción                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0B         | 0000000b-0cea-0010-8000-00aa00389b71<br/> Subtipo de KSDATAFORMAT \_ \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 bits, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby MAT 1,0:<br/> Dolby TrueHD (MLP – meridiano de embalaje sin pérdida) – 192KHz de 24 bits/hasta 18 Mbps, 8 canales) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby MAT 2,0: <br/> Dolby TrueHD: 192KHz de 24 bits/hasta 18 Mbps, 8 canales o LPCM hasta 24 Mbps. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ MAT21<br/> | Dolby MAT 2,1: <br/> Dolby TrueHD: 192KHz de 24 bits/hasta 18 Mbps, 8 canales o LPCM hasta 24 Mbps. <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ WMA \_ Pro<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

El controlador de clase de HD Audio proporcionado por Microsoft es compatible con los formatos PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT (MLP). Los GUID de los formatos de audio comprimidos que no son compatibles con el controlador de la clase HD audio y pueden ser implementados por soluciones de terceros se muestran en la tabla siguiente.



| CEA tipo 861 | GUID de subformato                                                                                              | Descripción                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ ATRAC<br/>           | Codificación acústica de transformación adaptable (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ audio de un \_ bit \_<br/> | One-Bit audio                                                                  |
| 0x0D         | 0000000d-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SubType \_ IEC61937 \_ DST<br/>             | Transporte de streaming directo (DST): DSD comprimido sin pérdida de conexión de streaming digital. |



 

## <a name="dolby-digital-plus-format"></a>Formato Dolby Digital Plus

Cuando el contenido de Dolby Digital Plus se transmite a través de IEC 60958, la velocidad de muestreo de vínculos debe ser cuatro veces la frecuencia de muestreo del contenido. Dolby Digital Plus admite velocidades de ejemplo de contenido de 32 KHz, 44,1 KHz y 48 KHz. Las interfaces como HDMI no admiten 128 KHz (32 KHz x 4), por lo que solo se pueden admitir las tasas de ejemplo de contenido 44,1 y 48 KHz.

En el ejemplo siguiente se muestran los valores establecidos por una aplicación de la \_ estructura WAVEFORMATEXTENSIBLE IEC61937 para representar el formato Dolby Digital Plus en una velocidad de muestra de contenido de 48 kHz.


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

El contenido de Dolby TrueHD se transmite a través de IEC 60958 a los canales de 176,4 kHz/8 (lo que requiere una velocidad de fotogramas IEC 60958 de 705,6 kHz) para la velocidad de ejemplo de contenido de los canales 44,1, 88,2 y 176,4 kHz y de 192 kHz/8 (que requiere una velocidad de fotogramas IEC 60958 de 768 kHz) para las velocidades de muestra de contenido

En los siguientes ejemplos se muestran los valores establecidos por una aplicación de la \_ estructura WAVEFORMATEXTENSIBLE IEC61937 para representar Dolby TrueHD en una velocidad de muestra de contenido de 96 kHz.

Dolby MAT 1,0


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



Dolby MAT 2,0


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



Dolby MAT 2,1


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
> La compatibilidad con una versión de Dolby MAT no implica la compatibilidad con Dolby MAT con un número de versión inferior. Dado que Dolby MAT 2,1 es compatible con versiones anteriores de Dolby MAT, un controlador de clase que indica la compatibilidad con Dolby MAT 2,1 normalmente también indicará la compatibilidad con Dolby MAT 2,0 y Dolby MAT 1,0, con una \_ estructura de WAVEFORMATEXTENSIBLE IEC61937 independiente para cada versión.

 

## <a name="wma-pro"></a>WMA Pro

El contenido de audio de WMA Pro se puede codificar en uno de los cuatro perfiles que aparecen en la tabla siguiente.



| Perfil | Valor de propiedad                                                                                                                                                                                                                                                      | Descripción                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Velocidad de bits máxima: 192000 bps <br/> Frecuencia de muestreo máxima: 48 KHz <br/> Número máximo de canales: 2 <br/> Tamaño máximo del búfer: 600 \* 1024 bits <br/> Muestras máximas por fotograma: 2048 <br/> Número máximo de bits por fotograma: 655536<br/>   | Recomendado para la música y la transmisión por secuencias de aire.<br/> La velocidad de bits máxima en un fotograma de audio es de 1536000 bps.<br/>          |
| M1      | Velocidad de bits máxima: 385000 bps <br/> Frecuencia de muestreo máxima: 48 KHz <br/> Número máximo de canales: 6 <br/> Tamaño máximo del búfer: 600 \* 1024 bits <br/> Muestras máximas por fotograma: 4096 <br/> Número máximo de bits por fotograma: 131072<br/>   | Recomendado para películas de definición estándar de sonido envolvente.<br/> La velocidad de bits máxima en un fotograma de audio es de 1536000 bps.<br/> |
| M2      | Velocidad de bits máxima: 769000 bps <br/> Frecuencia de muestreo máxima: 96 KHz <br/> Número máximo de canales: 6 <br/> Tamaño máximo del búfer: 1200 \* 1024 bits <br/> Muestras máximas por fotograma: 4096 <br/> Número máximo de bits por fotograma: 131072<br/>  | Recomendado para películas de alta definición con sonido envolvente.<br/> La velocidad máxima en un fotograma de audio es de 3072000 bps.<br/>         |
| M3      | Velocidad de bits máxima: 3 millones bps <br/> Frecuencia de muestreo máxima: 96 KHz <br/> Número máximo de canales: 8 <br/> Tamaño máximo del búfer: 2400 \* 1024 bits <br/> Muestras máximas por fotograma: 4096 <br/> Número máximo de bits por fotograma: 131072<br/> | Recomendado para el cine digital.<br/> La velocidad máxima en un fotograma de audio es de 3072000 bps.<br/>                               |



 

Los perfiles de M0 y M1 se encajan en una secuencia IEC 60958 de 48 KHz/16 bits/estéreo (1536000 bps). Los perfiles m2 y m3 caben en una secuencia IEC 60958 de 96 KHz/16 bits/estéreo (3072000 bps).

En el ejemplo siguiente se muestran los valores establecidos por una aplicación en la \_ estructura WAVEFORMATEXTENSIBLE IEC61937 para representar WMA Pro como perfil de m2.


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

 

 




