---
title: Origen de la imagen secundaria normal
description: Origen de la imagen secundaria normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- skins,button image source
- referencia de máscaras, botones
- botones en máscaras, origen de la imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967408"
---
# <a name="normal-secondary-image-source"></a>Origen de la imagen secundaria normal

Dependiendo de la función de botón, es posible que deba definir la ubicación de la imagen normal para el estado secundario del botón. Esta será la imagen que verán los usuarios cuando presionen un botón de función PlayPause la primera vez.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen normal para un origen de imagen secundario, si la imagen está dentro del mapa de bits Inserción, escriba:


```C++
Pushed @ 210,0

```



Los estados secundarios no pueden tener una imagen deshabilitada. Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




