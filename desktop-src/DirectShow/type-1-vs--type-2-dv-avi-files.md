---
description: Tipo 1 frente a
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Archivos AVI DV de tipo 1 frente a tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336aff4fed38e375bfc2f62d086ed103e076ed5fc54f85b80ea69cf389f82182
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633165"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Archivos AVI DV de tipo 1 frente a tipo 2

Las cámaras DV generan audio-vídeo intercalado; cada fotograma de vídeo también contiene la información de audio. Si guarda datos DV en un archivo AVI, puede elegir:

-   Almacene los datos intercalados como una secuencia en el archivo AVI. Esto se conoce como un archivo de tipo 1.
-   Divida los datos intercalados en secuencias de audio y vídeo independientes. Esto se conoce como un archivo de tipo 2.

Para la captura de vídeo, donde el rendimiento máximo es fundamental, es mejor usar un archivo de tipo 1, ya que los archivos de tipo 2 llevan datos de audio redundantes. (La secuencia de vídeo todavía tiene los datos de audio. El audio simplemente se oculta etiquetando la secuencia como vídeo). Además, la escritura de un archivo de tipo 2 requiere algún tiempo de procesador adicional para dividir la secuencia intercalada.

Por otro lado, los archivos de tipo 1 son menos eficaces para la edición en tiempo real. La aplicación debe extraer el audio de la secuencia intercalada, realizar las modificaciones e intercalar los datos de nuevo. Además, el formato de tipo 1 no es compatible con Microsoft® Video for Windows® (VFW). DirectShow puede controlar ambos tipos de archivos.

Un archivo de tipo 2 se puede convertir al tipo 1 mediante el filtro [DV Muxer.](dv-muxer-filter.md) Un archivo de tipo 1 se puede convertir al tipo 2 mediante el filtro [dv splitter.](dv-splitter-filter.md) En el diagrama siguiente se muestra la diferencia entre los dos formatos.

![conversión entre type-1 y type-2 dv](images/dv-filters3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Datos DV en formato de archivo AVI](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



