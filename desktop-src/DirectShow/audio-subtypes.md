---
description: En las tablas siguientes se muestran los GUID de subtipo multimedia para audio. Si procede, cada tabla muestra la etiqueta de formato equivalente, declarada en Mmreg.h.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Subtipos de audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162202"
---
# <a name="audio-subtypes"></a>Subtipos de audio

En las tablas siguientes se muestran los GUID de subtipo multimedia para audio. Si procede, cada tabla muestra la etiqueta de formato equivalente, declarada en Mmreg.h.

## <a name="uncompressed-audio-types"></a>Tipos de audio sin comprimir



| GUID                          | Descripción                | Encabezado  | Etiqueta de formato equivalente                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ FLOAT** | Audio de punto flotante IEEE. | uuids.h | **WAVE \_ FORMAT \_ IEEE \_ FLOAT** (0x0003) |
| **MEDIASUBTYPE \_ PCM**         | Audio PCM.                 | uuids.h | **WAVE \_ FORMAT \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>Tipos de audio MPEG-4 y AAC



| GUID                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Encabezado       | Etiqueta de formato equivalente                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Audio de codificación de audio avanzada (AAC) en formato Audio Data Transport Stream (ADTS).<br/> El bloque de formato es una [**estructura WAVEATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual a **WAVE FORMAT MPEG \_ \_ \_ ADTS \_ AAC**.<br/> La [**estructura WARPATEX**](/previous-versions/dd757713(v=vs.85)) especifica la frecuencia de muestreo principal de AAC-LC y el número de canales, antes de aplicar las herramientas de replicación de banda espectral (SBR) o estéreo paramétrico (PS), si están presentes.<br/> No se requieren datos adicionales después de la [**estructura DESATEX.**](/previous-versions/dd757713(v=vs.85))<br/>                                                                                                                                                                 | wmcodecdsp.h | **WAVE \_ FORMAT \_ MPEG \_ ADTS \_ AAC** (0x1600) |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | High-Efficiency secuencia de codificación de audio avanzada (HE-AAC).<br/> El bloque de formato es una [**estructura HEAACWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp.h | **WAVE \_ FORMAT \_ MPEG \_ HEAAC** (0x1610)     |
| **MEDIASUBTYPE \_ MPEG \_ LOAS**      | Flujo de transporte de audio MPEG-4 con una capa de sincronización (LOAS) y una capa multiplex (LATM).<br/> El bloque de formato es una [**estructura WAVEATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual a **WAVE FORMAT MPEG \_ \_ \_ LOAS**.<br/> La [**estructura WARPATEX**](/previous-versions/dd757713(v=vs.85)) especifica la frecuencia de muestreo principal de AAC-LC y el número de canales, antes de aplicar las herramientas SBR o PS espectrales, si están presentes.<br/> No se requieren datos adicionales después de la [**estructura DESATEX.**](/previous-versions/dd757713(v=vs.85))<br/>                                                                                                                                                                                             | wmcodecdsp.h | **WAVE \_ FORMAT \_ MPEG \_ LOAS** (0x1602)      |
| **MEDIASUBTYPE \_ RAW \_ AAC1**       | AAC sin procesar.<br/> El bloque de formato es una [**estructura WAVEATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual a **WAVE FORMAT RAW \_ \_ \_ AAC1**.<br/> La [**estructura DESATEX**](/previous-versions/dd757713(v=vs.85)) especifica la frecuencia de muestreo y el número de canales del audio descodificado después de aplicar las herramientas SBR y PS, si están presentes.<br/> La [**estructura DESATEX**](/previous-versions/dd757713(v=vs.85)) va seguida de bytes adicionales que contienen los datos de AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3 (MPEG-4 Audio). <br/> La longitud de los datos de AudioSpecificConfig() es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS. Es más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.<br/> | wmcodecdps.h | **WAVE \_ FORMAT \_ RAW \_ AAC1** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Tipos de audio Dolby



| GUID                                | Descripción                                                                                                                                                                                                             | Encabezado       | Etiqueta de formato equivalente                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ DOLBY \_ DDPLUS**     | Audio Dolby Digital Plus.                                                                                                                                                                                               | wmcodecdsp.h | N/D                                          |
| **MEDIASUBTYPE \_ DOLBY \_ AC3**        | Audio Dolby Digital (AC-3).                                                                                                                                                                                             | ksuuids.h    | N/D                                          |
| **MEDIASUBTYPE \_ DOLBY \_ AC3 \_ SPDIF** | Dolby AC-3 sobre S/PDIF.                                                                                                                                                                                                 | uuids.h      | **WAVE \_ FORMAT \_ DOLBY \_ AC3 \_ SPDIF** (0x0092) |
| **MEDIASUBTYPE \_ DVM**               | Códec DVM AC-3. Se usa al reproducir archivos AVI con audio Dolby Digital.<br/> El bloque de formato es una [**estructura WAVEATEX**](/previous-versions/dd757713(v=vs.85)) con la etiqueta de formato igual a **WAVE FORMAT \_ \_ DVM.**<br/> | wmcodecdsp.h | **WAVE \_ FORMAT \_ DVM** (0x2000)               |
| **MEDIASUBTYPE \_ RAW \_ SPORT**        | AC-3 sobre S/PDIF; vea Comentarios.                                                                                                                                                                                          | uuids.h      | **WAVE \_ FORMAT \_ RAW \_ SPORT** (0x0240)        |
| **MEDIASUBTYPE \_ SPDIF \_ TAG \_ 241h**  | AC-3 sobre S/PDIF; vea Comentarios.                                                                                                                                                                                          | uuids.h      | **WAVE \_ FORMAT \_ ESST \_ AC3** (0x0241)         |



 

Para especificar ac-3 agregado, use el subtipo **MEDIASUBTYPE \_ DOLBY \_ AC3 \_ SPDIF**, que corresponde a una etiqueta de formato de 0x0092 (WAVE \_ FORMAT DOLBY \_ \_ AC3 \_ SPDIF). Los valores 0x240 y 0x241 también se han usado para indicar ac-3 agregado, pero Microsoft fomenta el uso de 0x0092.

## <a name="miscellaneous-audio-types"></a>Tipos de audio varios



| GUID                                | Descripción                                                                                                                                                                                                                                                                          | Encabezado       | Etiqueta de formato equivalente           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **Audio DRM DE \_ MEDIASUBTYPE \_**        | Audio con protección de administración de derechos digitales (DRM).                                                                                                                                                                                                                               | uuids.h      | **WAVE \_ DRM \_ DE FORMATO** (0x0009)  |
| **MEDIASUBTYPE \_ DTS**               | Audio de Digital Theater Systems (DTS).<br/> El bloque de formato es una [**estructura WAVEATEX**](/previous-versions/dd757713(v=vs.85)) con la etiqueta de formato igual a **WAVE FORMAT \_ \_ UNKNOWN.**<br/>                                                                                              | ksuuids.h    | N/D                             |
| **MEDIASUBTYPE \_ DTS2**              | Audio de Digital Systems (DTS).<br/> El bloque de formato es una [**estructura DESATEX CON**](/previous-versions/dd757713(v=vs.85)) la etiqueta de formato igual a **WAVE FORMAT \_ \_ DTS2.**<br/> Este subtipo es equivalente a **MEDIASUBTYPE \_ DTS,** pero usa una etiqueta de formato diferente.<br/> | wmcodecdsp.h | **WAVE \_ FORMAT \_ DTS2** (0x2001) |
| **AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_**  | Datos de audio de DVD.                                                                                                                                                                                                                                                                      | ksuuids.h    | N/D                             |
| **MEDIASUBTYPE \_ MPEG1AudioPayload** | Carga de audio MPEG-1.                                                                                                                                                                                                                                                                | uuids.h      | **WAVE \_ FORMAT \_ MPEG** (0x0050) |
| **MEDIASUBTYPE \_ MPEG1Packet**       | Paquete de audio MPEG1.                                                                                                                                                                                                                                                                  | uuids.h      | N/D                             |
| **MEDIASUBTYPE \_ MPEG1Payload**      | Carga de audio MPEG1.                                                                                                                                                                                                                                                                 | uuids.h      | N/D                             |
| **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**      | Datos de audio MPEG-2.                                                                                                                                                                                                                                                                   | ksuuids.h    | N/D                             |



 

## <a name="audio-format-tags"></a>Etiquetas de formato de audio

El **campo wFormatTag** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica el tipo de formato de audio. Los ejemplos multimedia suelen ser un número completo de muestras, tal y como se especifica en el **campo wBitsPerSample** de la **estructura DESATEX.** Esto no es necesariamente cierto para las muestras de audio MPEG que pueden provienen de secuencias en paquetes y, por lo tanto, no se empaquetan necesariamente en límites de ejemplo o marco. Para el audio MPEG, la marca de tiempo de un ejemplo multimedia es la marca de tiempo del primer fotograma cuyo primer byte está contenido en el ejemplo multimedia.

Los subtipos de medios se definen para **cada wFormatTag** de la siguiente manera:

-   El subcampo Data1 del GUID del subtipo es el mismo que el **valor wFormatTag.**
-   El campo Data 2 es 0.
-   El campo Datos 3 es 0x0010.
-   El campo Data 4 es 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9B, 0x71.

Por lo tanto, para el audio PCM, el GUID del subtipo (definido en uuids.h como **MEDIASUBTYPE \_ PCM)** es:

`{00000001-0000-0010-8000-00AA00389B71}`

La [**función CreateAudioMediaType**](createaudiomediatype.md) se puede usar para crear una estructura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) a partir de una **estructura DE FORMA DEDATOS.**

## <a name="obsolete-audio-types"></a>Tipos de audio obsoletos

Los subtipos de audio siguientes están obsoletos y no se deben usar:

-   **MEDIASUBTYPE \_ MPEG \_ RAW \_ AAC**
-   **MEDIASUBTYPE \_ PCMAudioObsolete**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO \_ DE MEDIO \_ AM**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

