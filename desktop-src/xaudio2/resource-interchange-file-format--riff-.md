---
description: En esta introducción se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en archivos .wav. RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Formato de archivo para intercambio de recursos (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c223c5a1047ffc9828a42ccc09ce4a94f5e766a1bc4851996b911f15f90995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054335"
---
# <a name="resource-interchange-file-format-riff"></a>Formato de archivo para intercambio de recursos (RIFF)

En esta introducción se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en archivos .wav. RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.

## <a name="riff"></a>RIFF

Un archivo RIFF se compone de varias secciones discretas de datos *denominadas fragmentos*.

## <a name="fourcc-identifiers"></a>Identificadores FOURCC

El tipo de datos de un fragmento se indica mediante un identificador de código de cuatro caracteres (FOURCC). FOURCC es un entero de 32 bits sin signo creado mediante la concatenación de cuatro caracteres ASCII que se usan para identificar tipos de fragmentos en un archivo RIFF. Por ejemplo, fourcc "abcd" se representa en un sistema little-endian como 0x64636261. Los FOURCC pueden contener caracteres de espacio, por lo que "abc" es un FOURCC válido. Los archivos de audio usan códigos FOURCC para identificar fragmentos de formato de audio, fragmentos de datos de audio y cualquier otro fragmento específico del formato de audio.

En la tabla siguiente se muestran los identificadores FOURCC que se pueden esperar en los formatos de audio admitidos por XAudio2. 

| Formato | Identificadores FOURCC                     | Información adicional                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF", "fmt" , "data"                 |                                                                                                      |
| Adpcm  | "RIFF", "fmt", "data", "smpl", "wsmpl" | Consulte [Información general de ADPCM](adpcm-overview.md) para obtener una descripción de los identificadores FOURCC específicos de ADPCM. |



 

Los identificadores FOURCC "RIFF", "fmt" y "data" son comunes a todos los formatos admitidos. En la tabla siguiente se describen los identificadores FOURCC que se encuentran en todos los formatos admitidos. 

| Identificador FOURCC | Descripción                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Fragmento RIFF estándar que contiene un tipo de archivo con el valor "WAVE" o "XWMA" en los cuatro primeros bytes de su sección de datos y los otros fragmentos del archivo en el resto de su sección de datos.                                   |
| "fmt"             | Contiene el encabezado de formato del archivo de audio. Los datos de este fragmento se corresponden con una de las estructuras siguientes: **ESTAMÁQUELAATEX**, **ADPCMWAVEFORMAT DE ADPATEXTENSIBLE**.                                                  |
| "data"            | Contiene datos de audio para el archivo de audio. En XAudio2, el contenido del fragmento de datos se leerá en un búfer y se pasará a una voz de origen como miembro **pAudioData** de una estructura [**\_ BUFFER de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) |



 

## <a name="chunks"></a>Chunks

Un archivo RIFF consta de un fragmento de RIFF que contiene cero o más fragmentos.

-   El fragmento de RIFF tiene el formato siguiente:

    "RIFF", fileSize, fileType, data

    Donde "RIFF" es el código FOURCC literal "RIFF", *fileSize* es un valor de 4 bytes que da el tamaño de los datos del archivo y *fileType* es un FOURCC que identifica el tipo de archivo específico. El valor *de fileSize* incluye el tamaño de *fileType* FOURCC más el tamaño de los datos siguientes, pero no incluye el tamaño de "RIFF" FOURCC o el tamaño de *fileSize*. Los datos constan de fragmentos en cualquier orden.

-   Otros fragmentos tienen el formato siguiente:

    ```
    chunkID, chunkSize, data
    ```

    

    Donde *chunkID* es un FOURCC que identifica los datos contenidos en el fragmento, *chunkSize* es un valor de 4 bytes que proporciona el tamaño de la sección de datos del fragmento y los datos son cero o más bytes de datos. Los datos siempre se agregan al límite de WORD más cercano. *chunkSize* proporciona el tamaño de los datos válidos en el fragmento. No incluye el relleno, el tamaño de *chunkID* o el tamaño de *chunkSize.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Cómo: reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 



