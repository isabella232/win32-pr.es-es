---
description: Requisitos para descodificadores
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisitos para descodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362330"
---
# <a name="requirements-for-decoders"></a>Requisitos para descodificadores

Los descodificadores que entregan ejemplos a vmr deben observar las siguientes reglas:

-   Debe haber un fotograma de subaspección entregado a vmr para cada fotograma de vídeo. Los dos fotogramas deben tener las mismas marcas de tiempo.
-   Si el subpicture no ha cambiado, use la marca NOTASYNCPOINT de AM GBF en el método \_ \_ [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para forzar al asignador a devolver un búfer que contenga el último fotograma entregado a la VMR. Simplemente coloque una nueva marca de tiempo en el ejemplo y vuelva a entregarla a vmr. Si la subaspección está en blanco, todavía debe entregarla. El VMR detectará el fotograma vacío y no lo combinará con el vídeo. Esta prueba se realiza mediante el chip VGA y no afecta al rendimiento de reproducción.
-   Todos los ejemplos, excepto las secuencias en vivo, deben tener marcas de tiempo de inicio y de detenerse válidas asociadas. (El DVD no es un streaming en vivo).
-   Las marcas de tiempo de ejemplo de medios deben ser contiguas
-   El descodificador debe identificarse como compatible con VMR para que lo usen los generadores de grafos.
-   La secuencia de subimagen debe contener ahora valores alfa incrustados por píxel. El tipo de superficie ARGB4444 es ideal para subaspecciones.
-   No suponga que el paso de la subaspección es el mismo que el ancho de la superficie. Esto no siempre es así con vmr.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la aceleración de vídeo de DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



