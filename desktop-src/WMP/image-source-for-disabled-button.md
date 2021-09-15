---
title: Origen de la imagen para el botón Deshabilitado
description: Origen de la imagen para el botón Deshabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- skins,button image source
- referencia de máscaras, botones
- botones en máscaras, origen de la imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476224"
---
# <a name="image-source-for-disabled-button"></a>Origen de la imagen para el botón Deshabilitado

Debe definir el origen de la imagen que desea mostrar cuando un botón está deshabilitado o tiene un estado que corresponde a desactivado. La imagen procede del archivo que definió como Deshabilitado en la sección Mapas de bits. Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superior izquierdas (en píxeles) de la imagen que desea usar dentro del archivo de mapa de bits. La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón con respecto a la imagen de fondo, pero la ubicación de la que procede se define mediante los dos números siguientes a "Disabled @" y es relativa al mapa de bits Deshabilitado del que está leyendo la imagen.

Por ejemplo, para usar una imagen del mapa de bits Deshabilitado que se encuentra en el archivo Deshabilitado en una ubicación superior e izquierda de 50,60 píxeles, use el código siguiente:


```C++
Disabled @ 50,60

```



Debe definir un mapa de bits Deshabilitado. Si no desea mostrar una imagen diferente, puede definir el mapa de bits Fondo como el mapa de bits Deshabilitado con un desplazamiento de 0,0:


```C++
Disabled @ 50,60

```



En el ejemplo anterior, 50,60 es la ubicación del botón con el que está trabajando en el archivo deshabilitado (en este caso, la misma ubicación que el botón del mapa de bits Background). Sin embargo, se recomienda encarecidamente mostrar una imagen deshabilitada para todos los botones para proporcionar a los usuarios una indicación visual, ya que muchos botones no se podrán usar en determinadas condiciones, como una lista de reproducción vacía. Si los usuarios saben que un botón está deshabilitado, no seguirán intentando hacer clic en él ni pensarán que la máscara no funciona como está diseñada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




