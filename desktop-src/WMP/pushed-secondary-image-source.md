---
title: Origen de la imagen secundaria insertada
description: Origen de la imagen secundaria insertada
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075797"
---
# <a name="pushed-secondary-image-source"></a>Origen de la imagen secundaria insertada

Dependiendo de la función de botón, es posible que tenga que definir la ubicación de la imagen insertada para el estado secundario del botón. Será la imagen que verán los usuarios cuando inserten un botón de función PlayPause la segunda vez.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas de la parte superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de imagen del que está dibujando.

Por ejemplo, para definir la imagen insertada para un origen de imagen secundario, si la imagen está dentro del mapa de bits insertado, escriba:


```C++
Pushed @ 248,0

```



Los Estados secundarios no pueden tener una imagen deshabilitada. Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




