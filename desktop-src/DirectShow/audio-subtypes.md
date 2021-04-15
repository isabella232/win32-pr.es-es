---
description: En las tablas siguientes se enumeran los GUID de subtipo de medios para audio. Cuando sea aplicable, cada tabla muestra la etiqueta de formato equivalente, que se declara en Mmreg. h.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Subtipos de audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494933"
---
# <a name="audio-subtypes"></a>Subtipos de audio

En las tablas siguientes se enumeran los GUID de subtipo de medios para audio. Cuando sea aplicable, cada tabla muestra la etiqueta de formato equivalente, que se declara en Mmreg. h.

## <a name="uncompressed-audio-types"></a>Tipos de audio sin comprimir



| GUID                          | Descripción                | Encabezado  | Etiqueta de formato equivalente                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ float** | Audio de punto flotante IEEE. | UUID. h | **Wave \_ FORMATO \_ IEEE \_ float** (0x0003) |
| **MEDIASUBTYPE \_ PCM**         | Audio PCM.                 | UUID. h | **Wave \_ FORMATO \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>Tipos de audio MPEG-4 y AAC



| GUID                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Encabezado       | Etiqueta de formato equivalente                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Audio AAC (codificación de audio avanzado) en formato de flujo de transporte de datos de audio (ADTS).<br/> El bloque Format es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual al **\_ formato Wave \_ MPEG \_ ADTS \_ AAC**.<br/> La estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica la velocidad de muestreo AAC-LC básica y el número de canales, antes de aplicar las herramientas de replicación de banda espectral (SBR) o estéreo paramétricos (PS), si está presente.<br/> No se necesitan datos adicionales después de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                 | wmcodecdsp. h | **Wave \_ FORMATO de \_ MPEG \_ ADTS \_ AAC** (0x1600) |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | High-Efficiency secuencia de codificación de audio avanzada (HE-AAC).<br/> El bloque Format es una estructura [**HEAACWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp. h | **Wave \_ FORMATO \_ MPEG \_ HEAAC** (0x1610)     |
| **MEDIASUBTYPE \_ MPEG \_ loa**      | Secuencia de transporte de audio MPEG-4 con una capa de sincronización (Loa) y una capa de multiplexación (LATM).<br/> El bloque Format es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual al **\_ formato Wave \_ MPEG \_ loa**.<br/> La estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica la velocidad de ejemplo de AAC-LC básica y el número de canales, antes de aplicar las herramientas SBR o PS de espectral, si está presente.<br/> No se necesitan datos adicionales después de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                                             | wmcodecdsp. h | **Wave \_ FORMATO \_ MPEG \_ loa** (0x1602)      |
| **MEDIASUBTYPE \_ raw \_ AAC1**       | AAC sin procesar.<br/> El bloque de formato es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** igual al **formato de onda \_ \_ \_ AAC1 RAW**.<br/> La estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica la velocidad de muestreo y el número de canales en el audio descodificado después de aplicar las herramientas SBR y PS, si están presentes.<br/> La estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) va seguida de bytes adicionales que contienen los datos AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3 (audio MPEG-4). <br/> La longitud de los datos AudioSpecificConfig () es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS. Tiene más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.<br/> | wmcodecdps. h | **Wave \_ FORMAT \_ raw \_ AAC1** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Tipos de audio Dolby



| GUID                                | Descripción                                                                                                                                                                                                             | Encabezado       | Etiqueta de formato equivalente                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ Dolby \_ DDPLUS**     | Audio Dolby Digital Plus.                                                                                                                                                                                               | wmcodecdsp. h | N/D                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3**        | Audio Dolby Digital (AC-3).                                                                                                                                                                                             | ksuuids. h    | N/D                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3 ( \_ SPDIF)** | Dolby AC-3 sobre S/PDIF.                                                                                                                                                                                                 | UUID. h      | **Wave \_ FORMATEAr \_ Dolby \_ AC3 \_ SPDIF** (0x0092) |
| **MEDIASUBTYPE \_ DVM**               | Códec AC-3 de DVM. Se usa al reproducir archivos AVI con audio Dolby digital.<br/> El bloque de formato es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con la etiqueta de formato igual al **formato de onda \_ \_ DVM**.<br/> | wmcodecdsp. h | **Wave \_ FORMATO \_ DVM** (0x2000)               |
| **\_deportes bruto de MEDIASUBTYPE \_**        | AC-3 sobre S/PDIF; Vea la sección Comentarios.                                                                                                                                                                                          | UUID. h      | **Wave \_ DAR formato al \_ \_ deporte crudo** (0x0240)        |
| **MEDIASUBTYPE \_ \_ 241h de etiqueta SPDIF \_**  | AC-3 sobre S/PDIF; Vea la sección Comentarios.                                                                                                                                                                                          | UUID. h      | **Wave \_ FORMAT \_ ESST \_ AC3** (0x0241)         |



 

Para especificar AC-3 rellenado, use el subtipo **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF**, que corresponde a una etiqueta de formato de 0x0092 (formato de onda \_ \_ Dolby \_ AC3 de \_ SPDIF). Los valores 0x240 y 0x241 también se han utilizado para indicar AC-3 rellenado, pero Microsoft recomienda el uso de 0x0092.

## <a name="miscellaneous-audio-types"></a>Tipos de audio varios



| GUID                                | Descripción                                                                                                                                                                                                                                                                          | Encabezado       | Etiqueta de formato equivalente           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **\_Audio DRM de MEDIASUBTYPE \_**        | Audio con protección de administración de derechos digitales (DRM).                                                                                                                                                                                                                               | UUID. h      | **Wave \_ FORMATO de \_ DRM** (0x0009)  |
| **MEDIASUBTYPE \_ DTS**               | Audio de sistemas de Digital Theater (DTS).<br/> El bloque Format es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con la etiqueta de formato igual al **formato de onda \_ \_ Unknown**.<br/>                                                                                              | ksuuids. h    | N/D                             |
| **MEDIASUBTYPE \_ DTS2**              | Audio de sistemas de Digital Theater (DTS).<br/> El bloque de formato es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con la etiqueta de formato igual al **formato de onda \_ \_ DTS2**.<br/> Este subtipo es equivalente a **MEDIASUBTYPE \_ DTS** , pero usa una etiqueta de formato diferente.<br/> | wmcodecdsp. h | **Wave \_ FORMATO de \_ DTS2** (0x2001) |
| **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**  | Datos de audio de DVD.                                                                                                                                                                                                                                                                      | ksuuids. h    | N/D                             |
| **MEDIASUBTYPE \_ MPEG1AudioPayload** | Carga de audio MPEG-1.                                                                                                                                                                                                                                                                | UUID. h      | **Wave \_ FORMATO \_ MPEG** (0x0050) |
| **MEDIASUBTYPE \_ MPEG1Packet**       | Paquete de audio de MPEG1.                                                                                                                                                                                                                                                                  | UUID. h      | N/D                             |
| **MEDIASUBTYPE \_ MPEG1Payload**      | Carga de audio MPEG1.                                                                                                                                                                                                                                                                 | UUID. h      | N/D                             |
| **\_Audio MPEG2 de MEDIASUBTYPE \_**      | Datos de audio MPEG-2.                                                                                                                                                                                                                                                                   | ksuuids. h    | N/D                             |



 

## <a name="audio-format-tags"></a>Etiquetas de formato de audio

El campo **wFormatTag** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica el tipo de formato de audio. Los ejemplos de medios suelen ser un número entero de muestras, tal como se especifica en el campo **wBitsPerSample** de la estructura **WAVEFORMATEX** . Esto no es necesariamente así en el caso de las muestras de audio MPEG que pueden proviene de secuencias empaquetadas y, por lo tanto, no están necesariamente empaquetados en límites de muestras o fotogramas. En el caso de MPEG Audio, la marca de tiempo de un ejemplo multimedia es la marca de tiempo para el primer fotograma cuyo primer byte está incluido en el ejemplo multimedia.

Los subtipos de medios se definen para cada **wFormatTag** como se indica a continuación:

-   El subcampo data1 del GUID del subtipo es igual que el valor de **wFormatTag** .
-   El campo data 2 es 0.
-   El campo data 3 es 0x0010.
-   El campo data 4 es 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9B, 0x71.

Por lo tanto, para audio PCM el GUID del subtipo (definido en UUID. h como **MEDIASUBTYPE \_ PCM**) es:

`{00000001-0000-0010-8000-00AA00389B71}`

La función [**CreateAudioMediaType**](createaudiomediatype.md) se puede usar para crear una estructura de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a partir de una estructura **WAVEFORMATEX** .

## <a name="obsolete-audio-types"></a>Tipos de audio obsoletos

Los siguientes subtipos de audio están obsoletos y no se deben usar:

-   **MEDIASUBTYPE \_ MPEG \_ raw \_ AAC**
-   **MEDIASUBTYPE \_ PCMAudioObsolete**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de medio am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

