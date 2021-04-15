---
title: Origen de imagen secundaria normal
description: Origen de imagen secundaria normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695433"
---
# <a name="normal-secondary-image-source"></a>Origen de imagen secundaria normal

Dependiendo de la función de botón, es posible que tenga que definir la ubicación de la imagen normal para el estado secundario del botón. Será la imagen que verán los usuarios cuando inserten un botón de función PlayPause la primera vez.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen normal para un origen de imagen secundario, si la imagen está dentro del mapa de bits insertado, escriba:


```C++
Pushed @ 210,0

```



Los Estados secundarios no pueden tener una imagen deshabilitada. Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




