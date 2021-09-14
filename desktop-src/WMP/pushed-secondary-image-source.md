---
title: Origen de la imagen secundaria inserda
description: Origen de la imagen secundaria inserda
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073230"
---
# <a name="pushed-secondary-image-source"></a>Origen de la imagen secundaria inserda

Dependiendo de la función de botón, es posible que tenga que definir la ubicación de la imagen presionada para el estado secundario del botón. Esta será la imagen que verán los usuarios cuando presionen un botón de función PlayPause la segunda vez.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superiores izquierdas (en píxeles) de la imagen que desea usar dentro del tipo de imagen del que está dibujando.

Por ejemplo, para definir la imagen pushed para un origen de imagen secundario, si la imagen está dentro del mapa de bits Pushed , escriba:


```C++
Pushed @ 248,0

```



Los estados secundarios no pueden tener una imagen deshabilitada. Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




