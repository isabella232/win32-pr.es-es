---
description: Muestra cómo usar Microsoft Media Foundation para descodificar el audio de un archivo multimedia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Ejemplo de clip de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686472"
---
# <a name="audio-clip-sample"></a>Ejemplo de clip de audio

Muestra cómo usar Microsoft Media Foundation para descodificar el audio de un archivo multimedia.

La aplicación de ejemplo de clip de audio Lee los datos de audio de un archivo multimedia y escribe el audio sin comprimir en un archivo de onda.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Uso

Este ejemplo es una aplicación de línea de comandos. Usa los siguientes argumentos de línea de comandos:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   ArchivoDeEntrada: el nombre de un archivo que contiene una secuencia de audio.
-   OutputFile. wav: nombre del archivo de onda que se va a escribir.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Tutorial: descodificar audio](tutorial--decoding-audio.md)
</dt> </dl>

 

 



