---
description: La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminancia.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminación de HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274607"
---
# <a name="hdr-lighting-direct3d-9"></a>Iluminación de HDR (Direct3D 9)

La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminancia. El mundo real tiene aproximadamente 10 pedidos de intervalo dinámico (DR) para los valores de luminancia distribuidos en el espectro de oscuridad al brillo. Por otro lado, una pantalla de equipo tiene una gama de pantalla muy limitada (o un intervalo de valores de luminancia): aproximadamente dos pedidos de intervalo dinámico. El reto de producir imágenes representadas de HDR es asignar los valores de HDR del mundo real en la gama limitada de la pantalla de un equipo.

La asignación de tono es la técnica que usa DirectX para asignar información de HDR a un intervalo más limitado. La asignación de tono aplicada a la representación en CGI puede mejorar drásticamente la cantidad de detalles de iluminación representada, lo que permite ver los detalles en las áreas más oscuras y proporcionar un contraste en las áreas que son tan brillantes, que aparecen grabadas. Las escenas resultantes se representan con detalles de iluminación mucho más visibles.

El [ejemplo HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) es un ejemplo de SDK que muestra la iluminación HDR.

## <a name="tone-mapping"></a>Asignación de tono

Normalmente, la asignación de tono simula los fenómenos ópticos que no pueden ser causados por la recuperación ante desastres del monitor. Ejemplos de esto son los destellos o la floración (que son principalmente propiedades de lentes), el turno azul que ocurre en el ojo humano en condiciones de poca luz y otras adaptaciones que son el resultado de la bioquímica del ojo. Si la recuperación ante desastres de la pantalla era lo suficientemente grande, la asignación de tono no sería tan necesaria, salvo para proporcionar efectos artísticos o algunas de las propiedades de una lente de la cámara o un dispositivo acoplado a carga (CCD).

La asignación de tono divide el intervalo de valores de luminancia de una escena en un conjunto de zonas. Cada zona abarca un intervalo de valores de luminancia.

HDR usa los siguientes términos:

-   Zona-intervalo de valores de luminancia
-   Región de brillo central gris de la escena
-   Intervalo dinámico: relación entre la luminancia de la escena más alta y la luminancia de la escena más baja
-   Medición clave-subjetiva de la iluminación de la escena: varía de una luz a una moderada

Para calcular la luminancia a partir de los valores RGB, use lo siguiente:


```
L = 0.27R + 0.67G + 0.06B;
```



La luminancia media del registro es una aproximación útil para la clave de una escena. Una ecuación general tiene el siguiente aspecto:

L<sub>w</sub> = exp \[ 1/N (registro de suma \[ (delta + L<sub>w</sub>(x, y)) \] ) \]

Donde:

-   L<sub>registro-promedio de luminancia</sub>
-   N: número de píxeles de la imagen
-   Delta: un pequeño factor para evitar problemas con los píxeles negros
-   L<sub>w</sub>(x, y): la luminancia del espacio mundial del píxel (x, y)

Para asignarlo a un valor de gris medio, este es un operador de escala de luminancia:

L (x, y) = a \* l<sub>w</sub>(x, y)/L<sub>w</sub>

Donde:

-   L (x, y): luminancia escalada para píxel (x, y)
-   un valor de clave-Image después de aplicar el ajuste de escala

Y, por último, aquí se muestra un operador de asignación de tono simple para comprimir el luminances alto:

L<sub>d</sub>(x, y) = L (x, y)/(1 + L (x, y))

Donde:

-   L<sub>d</sub>(x, y): luminancia comprimida y escalada para el píxel (x, y)
-   un valor de clave-Image después de aplicar el ajuste de escala

Este operador escala luminances alto en 1/L y luminances inferior en 1. Para obtener más información, consulte el siguiente documento.

Reinhard, Erik, Mike, Peter Shirley y James Ferwerda. ["Reproducción de tonos fotográficos para imágenes digitales"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf). Transacciones ACM en gráficos (TOG), procedimientos de la campaña 29 de la Conferencia sobre gráficos de equipos y técnicas interactivas (SIGGRAPH), PP. 267-276. Nueva York, NY: ACM Press, 2002.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 



