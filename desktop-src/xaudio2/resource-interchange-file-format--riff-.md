---
description: En esta información general se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en los archivos. wav. RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Formato de archivo para intercambio de recursos (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717140"
---
# <a name="resource-interchange-file-format-riff"></a>Formato de archivo para intercambio de recursos (RIFF)

En esta información general se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en los archivos. wav. RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.

## <a name="riff"></a>RIFF

Un archivo RIFF se compone de varias secciones discretas de datos denominados *fragmentos*.

## <a name="fourcc-identifiers"></a>Identificadores FOURCC

El tipo de datos de un fragmento se indica mediante un identificador de código de cuatro caracteres (FOURCC). Un FOURCC es un entero sin signo de 32 bits creado mediante la concatenación de cuatro caracteres ASCII que se usan para identificar tipos de fragmentos en un archivo RIFF. Por ejemplo, el FOURCC "ABCD" se representa en un sistema Little-Endian como 0x64636261. FOURCCs puede contener caracteres de espacio, por lo que "ABC" es un FOURCC válido. Los archivos de audio usan códigos FOURCC para identificar fragmentos de formato de audio, fragmentos de datos de audio y cualquier otro fragmento específico del formato de audio.

En la tabla siguiente se muestran los identificadores FOURCC que se pueden esperar en los formatos de audio admitidos por XAudio2. 

| Formato | Identificadores FOURCC                     | Información adicional                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF", "FMT", "Data"                 |                                                                                                      |
| ADPCM  | "RIFF", "FMT", "Data", "smpl", "wsmpl" | Consulte [información general de ADPCM](adpcm-overview.md) para obtener una descripción de los identificadores FourCC específicos de ADPCM. |



 

Los identificadores de FOURCC "RIFF", "FMT" y "Data" son comunes a todos los formatos admitidos. En la tabla siguiente se describen los identificadores FOURCC que se encuentran en todos los formatos admitidos. 

| Identificador FOURCC | Descripción                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Fragmento RIFF estándar que contiene un tipo de archivo con el valor "WAVE" o "XWMA" en los primeros cuatro bytes de su sección de datos y los demás fragmentos del archivo en el resto de los datos.                                   |
| "fmt"             | Contiene el encabezado de formato del archivo de audio. Los datos de este fragmento se corresponden con una de las siguientes estructuras: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contiene datos de audio para el archivo de audio. En XAudio2, el contenido del fragmento de datos se leerá en un búfer y se pasará a una voz de origen como el miembro **pAudioData** de una estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . |



 

## <a name="chunks"></a>Chunks

Un archivo RIFF se compone de un fragmento RIFF que contiene cero o más fragmentos.

-   El fragmento RIFF tiene el formato siguiente:

    "RIFF", archivo, fileType, datos

    Donde "RIFF" es el código de FOURCC literal "RIFF" *, el tamaño de archivo es* un valor de 4 bytes que asigna el tamaño de los datos en el archivo y *FILETYPE* es un FourCC que identifica el tipo de archivo específico. El valor de *fileing* incluye el tamaño de *filetype* FourCC más el tamaño de los datos siguientes, pero no incluye el tamaño del FourCC "Riff" o el tamaño de *los archivos*. Los datos se componen de fragmentos en cualquier orden.

-   Otros fragmentos tienen el formato siguiente:

    ```
    chunkID, chunkSize, data
    ```

    

    Donde *chunkID* es un FourCC que identifica los datos contenidos en el fragmento, *chunkSize* es un valor de 4 bytes que asigna el tamaño de la sección de datos del fragmento y los datos son cero o más bytes de datos. Los datos siempre se rellenan hasta el límite de palabras más cercano. *chunkSize* proporciona el tamaño de los datos válidos en el fragmento. No incluye el relleno, el tamaño de *chunkID* o el tamaño de *chunkSize*.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Cómo: reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 



