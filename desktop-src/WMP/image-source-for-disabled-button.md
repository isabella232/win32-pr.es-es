---
title: Origen de imagen para botón deshabilitado
description: Origen de imagen para botón deshabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418727"
---
# <a name="image-source-for-disabled-button"></a>Origen de imagen para botón deshabilitado

Debe definir el origen de la imagen que desea mostrar cuando un botón está deshabilitado o tiene un estado que corresponde a desactivado. La imagen procede del archivo definido como deshabilitado en la sección mapas de bits. Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del archivo de mapa de bits. La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón en relación con la imagen de fondo, pero la ubicación desde la que procede se define mediante los dos números que siguen a "Disabled @" y es relativo al mapa de bits deshabilitado del que se lee la imagen.

Por ejemplo, para usar una imagen del mapa de bits deshabilitado que se encuentra en el archivo deshabilitado en una ubicación superior e izquierda de 50, 60 píxeles, use el código siguiente:


```C++
Disabled @ 50,60

```



Debe definir un mapa de bits deshabilitado. Si no desea mostrar una imagen diferente, puede definir el mapa de bits de fondo como el mapa de bits deshabilitado con un desplazamiento de 0, 0:


```C++
Disabled @ 50,60

```



En el ejemplo anterior, 50, 60 es la ubicación del botón con el que está trabajando en el archivo deshabilitado (en este caso, la misma ubicación que el botón en el mapa de bits de fondo). Sin embargo, se recomienda encarecidamente mostrar una imagen deshabilitada para todos los botones a fin de que los usuarios tengan una indicación visual, ya que no se podrán usar muchos botones en determinadas condiciones, como una lista de reproducción vacía. Si los usuarios saben que un botón está deshabilitado, no seguirán intentando hacer clic en él o piensa que la piel no funciona según lo previsto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




