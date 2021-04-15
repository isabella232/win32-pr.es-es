---
description: Requisitos para descodificadores
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisitos para descodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494842"
---
# <a name="requirements-for-decoders"></a>Requisitos para descodificadores

Los descodificadores que proporcionan ejemplos a la VMR deben observar las siguientes reglas:

-   Debe haber un fotograma de subimagen entregado al VMR para cada fotograma de vídeo. Los dos fotogramas deben tener las mismas marcas de tiempo.
-   Si la subimagen no ha cambiado, use la \_ marca AM GBF \_ NOTASYNCPOINT en el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obligar al asignador a que devuelva un búfer que contenga el último fotograma entregado a VMR. Simplemente coloque una nueva marca de tiempo en el ejemplo y entréguela de nuevo a la VMR. Si la fama de la subimagen está en blanco, debe proporcionarla. VMR detectará el fotograma vacío y no lo combinará con el vídeo. Esta prueba se realiza mediante el chip VGA y no afecta al rendimiento de la reproducción.
-   Todos los ejemplos, a excepción de las secuencias en directo, deben tener marcas de tiempo de inicio y detención válidas adjuntas. (El DVD no es una secuencia en directo).
-   Las marcas de tiempo de ejemplo multimedia deben ser contiguas
-   El descodificador debe identificarse como compatible con VMR para su uso por los generadores de gráficos.
-   La secuencia de subimagen ahora debe contener valores alfa por píxel incrustados. El tipo de superficie ARGB4444 es ideal para las subimágenes.
-   No suponga que el paso de la subimagen es el mismo que el ancho de la superficie. Este no es siempre el caso de la VMR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo sobre DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



