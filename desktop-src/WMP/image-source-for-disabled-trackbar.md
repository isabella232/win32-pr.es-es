---
title: Origen de imagen para TrackBar deshabilitado
description: Origen de imagen para TrackBar deshabilitado
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, origen de imagen
- origen de imagen para máscaras, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695320"
---
# <a name="image-source-for-disabled-trackbar"></a>Origen de imagen para TrackBar deshabilitado

Debe definir el origen de la imagen que desea mostrar cuando se deshabilita una barra de información mediante el tipo de mapa de bits del que desea dibujar la imagen. La imagen que se muestra normalmente estará dentro del superarchivo o si está creando una máscara para Windows Media Player 10 Mobile, la imagen estará dentro del archivo SeekThumb. Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para usar una imagen del mapa de bits SeekThumb que tiene una posición superior e izquierda de 50, 60 píxeles, escriba:


```C++
Disabled @ 50,60

```



Debe definir una ubicación de imagen para una imagen de TrackBar deshabilitada. Si no desea mostrar una nueva imagen, puede definir la imagen de fondo como la imagen deshabilitada con un desplazamiento de 0, 0:


```C++
Disabled @ 50,60

```



En el ejemplo anterior, 50, 60 representa la ubicación del botón con el que está trabajando en el archivo SeekThumb (en este caso, la misma ubicación que el botón en el mapa de bits de fondo). Sin embargo, se recomienda encarecidamente mostrar una imagen deshabilitada para todos los trackbars para que el usuario tenga una indicación visual, porque trackbars no se podrá usar en determinadas condiciones. Por ejemplo, la búsqueda de trackbars puede estar deshabilitada si la lista de reproducción actual está vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




