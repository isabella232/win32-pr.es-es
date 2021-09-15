---
description: La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminosidad.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminación HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465377"
---
# <a name="hdr-lighting-direct3d-9"></a>Iluminación HDR (Direct3D 9)

La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminosidad. El mundo real tiene unos 10 pedidos de intervalo dinámico (DR) para los valores de luminosidad repartidos por el espectro de temperatura hasta el brillo. Por otro lado, una pantalla de equipo tiene una gama de pantalla muy limitada (o intervalo de valores de luminosidad): aproximadamente dos pedidos de intervalo dinámico. El desafío de producir imágenes representados por HDR es asignar los valores DE HDR del mundo real a la gama limitada de una pantalla de equipo.

La asignación de tono es la técnica que usa DirectX para asignar información DE HDR a un intervalo más limitado. La asignación de tono aplicada a la representación de CGI puede mejorar considerablemente la cantidad de detalles de iluminación representados, lo que permite ver los detalles de las áreas más oscuras y proporcionar contraste en las áreas que son tan brillantes que parecen amanecer. Las escenas resultantes se representan con detalles de iluminación mucho más visibles.

[El ejemplo HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) es un ejemplo de SDK que muestra la iluminación HDR.

## <a name="tone-mapping"></a>Asignación de tono

Por lo general, la asignación de tono simula fenómenos ópticos que no pueden deberse a la recuperación ante desastres del monitor. Algunos ejemplos de esto son los cascos o las gafas (que son principalmente propiedades de las lentes), el cambio azul que se produce en el ojo humano en condiciones de poca luz y otras adaptaciones que son el resultado de la bioquímico del ojo. Si la recuperación ante desastres de la pantalla fuera lo suficientemente grande, la asignación de tono no sería tan necesaria, excepto para proporcionar efectos de efecto óptico o algunas de las propiedades de una lente de cámara o un dispositivo acoplado a carga (CCD).

La asignación de tono divide el intervalo de valores de luminosidad de una escena en un conjunto de zonas. Cada zona abarca un intervalo de valores de luminosidad.

HDR usa los términos siguientes:

-   Zona: intervalo de valores de luminosidad
-   Gris medio: región de brillo medio de la escena
-   Intervalo dinámico: proporción de la luminosidad de escena más alta con la luminosidad de la escena más baja
-   Clave: medición subjetiva de la iluminación de la escena: varía de ligera a moderada a oscura

Para calcular la luminosidad a partir de valores RGB, use lo siguiente:


```
L = 0.27R + 0.67G + 0.06B;
```



La luminosidad de promedio de registro es una aproximación útil para la clave de una escena. Una ecuación general tiene este aspecto:

L<sub>w</sub> = exp \[ 1 / N( sum \[ log( delta + L<sub>w</sub>( x, y ) ) \] ) ) \]

Donde:

-   L<sub>w</sub> : luminosidad de promedio de registro
-   N: número de píxeles de la imagen
-   delta: un factor pequeño para evitar problemas con píxeles negros
-   L<sub>w</sub>( x, y ) - la luminosidad del espacio mundial para píxeles ( x, y )

Para asignarlo a un valor gris medio, este es un operador de escalado de luminosidad:

L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub>

Donde:

-   L( x, y ) - luminosidad escalada para píxeles ( x, y )
-   un valor de clave de imagen después de aplicar el escalado

Y, por último, este es un operador de asignación de tono simple para comprimir las altas luminosidads:

L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )

Donde:

-   L<sub>d</sub>( x, y ) - luminosidad comprimida y escalada para píxeles ( x, y )
-   un valor de clave de imagen después de aplicar el escalado

Este operador escala las luminosidads altas en 1/L y las luminosidads bajas en 1. Para más información, consulte el siguiente documento.

Reinhard, Erik, Mike Mike, Peter Petery y James Peterwerda. ["La reproducción del tono de la fotografía para imágenes digitales".](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf) ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276. Nueva York, NY: ACM Press, 2002.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 



