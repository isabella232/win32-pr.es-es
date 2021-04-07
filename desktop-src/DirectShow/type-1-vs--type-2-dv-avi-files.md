---
description: Escriba-1 frente a
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Archivos AVI de tipo 1 frente a-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002153"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Archivos AVI de tipo 1 frente a-2

Las cámaras DV producen audio y vídeo intercalados; cada fotograma de vídeo también contiene la información de audio. Si guarda los datos de DV en un archivo AVI, tendrá una opción:

-   Almacene los datos intercalados como una secuencia en el archivo AVI. Esto se conoce como archivo de tipo 1.
-   Divida los datos intercalados en secuencias de audio y vídeo independientes. Esto se conoce como archivo de tipo 2.

Para la captura de vídeo, donde el rendimiento máximo es fundamental, es mejor usar un archivo de tipo 1, ya que los archivos de tipo 2 llevan datos de audio redundantes. (El flujo de vídeo todavía tiene los datos de audio. El audio se oculta simplemente mediante la etiqueta de la secuencia como vídeo.) Además, la escritura de un archivo de tipo 2 requiere tiempo adicional de procesador para dividir el flujo intercalado.

Por otro lado, los archivos de tipo 1 son menos eficientes para la edición en tiempo real. La aplicación debe extraer el audio del flujo intercalado, realizar las modificaciones y volver a intercalar los datos. Además, el formato de tipo 1 no es compatible con Microsoft® vídeo para Windows® (VFW). DirectShow puede controlar ambos tipos de archivos.

Un archivo de tipo 2 se puede convertir al tipo-1 mediante el filtro [DV multiplexor](dv-muxer-filter.md) . Un archivo de tipo 1 se puede convertir al tipo 2 mediante el filtro de [divisor DV](dv-splitter-filter.md) . En el diagrama siguiente se ilustra la diferencia entre los dos formatos.

![conversión entre el tipo 1 y el tipo-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Datos de DV en el formato de archivo AVI](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



