---
title: Origen de la imagen insertada
description: Origen de la imagen insertada
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777089"
---
# <a name="pushed-image-source"></a>Origen de la imagen insertada

Debe definir el origen de la imagen que desea mostrar cuando el usuario presiona un botón. La imagen procede del archivo que definió como insertada en la sección mapas de bits. Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior e izquierda (en píxeles) de la imagen que desea usar dentro del archivo de imagen insertado. La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón en relación con la imagen de fondo. pero la ubicación desde la que procede se define mediante los dos números que siguen a "push @" y es relativo a la imagen insertada de la que está leyendo la imagen.

Por ejemplo, para usar una imagen de la imagen insertada que se encuentra en el archivo insertado cuya ubicación superior izquierda es 50, 60 usaría el siguiente código:


```C++
Pushed @ 50,60

```



Si no desea mostrar una imagen diferente, puede definir el mapa de bits de fondo como mapa de bits insertado. Para ello, especifique el archivo de fondo como el archivo insertado y especifique el desplazamiento en la esquina superior izquierda del botón:


```C++
Pushed @ 50,60

```



Si lo hace, ninguno de los botones puede mostrar una imagen insertada. Se recomienda mostrar una imagen insertada para todos los botones con el fin de proporcionar una indicación visual al usuario, ya que no siempre está claro si una derivación produce un resultado, especialmente cuando se está reproduciendo música o se desactiva el sonido punteo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




