---
title: Origen de la imagen para la barra de seguimiento deshabilitada
description: Origen de la imagen para la barra de seguimiento deshabilitada
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Reproductor de Windows Media Máscaras móviles, barras de seguimiento
- máscaras, barras de seguimiento
- referencia de máscaras, barras de seguimiento
- barras de seguimiento en máscaras, origen de imagen
- origen de imagen para máscaras, barras de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b3f5f58198d55f2dcd17b23b102c91eb4dff4787489e13775c6be71faa3223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338950"
---
# <a name="image-source-for-disabled-trackbar"></a>Origen de la imagen para la barra de seguimiento deshabilitada

Debe definir el origen de la imagen que desea mostrar cuando se deshabilita una barra de seguimiento, con el tipo de mapa de bits del que desea dibujar la imagen. La imagen que se muestra normalmente estará dentro del archivo Super o, si va a crear una máscara para Reproductor de Windows Media 10 Mobile, la imagen estaría dentro del archivo SeekThumb. Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para usar una imagen del mapa de bits SeekThumb que tenga una posición superior e izquierda de 50,60 píxeles, escriba:


```C++
Disabled @ 50,60

```



Debe definir una ubicación de imagen para una imagen de barra de seguimiento deshabilitada. Si no desea mostrar una imagen nueva, puede definir la imagen de fondo como la imagen deshabilitada con un desplazamiento de 0,0:


```C++
Disabled @ 50,60

```



En el ejemplo anterior, 50,60 representa la ubicación del botón con el que está trabajando en el archivo SeekThumb (en este caso, la misma ubicación que el botón del mapa de bits Background). Sin embargo, se recomienda encarecidamente que muestre una imagen deshabilitada para todas las barras de seguimiento para proporcionar al usuario una indicación visual, ya que las barras de seguimiento no se podrán usar en determinadas condiciones. Por ejemplo, buscar barras de seguimiento puede deshabilitarse cuando la lista de reproducción actual está vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Barras de seguimiento**](trackbars.md)
</dt> </dl>

 

 




