---
title: Origen de imagen terciaria inserda
description: Origen de imagen terciaria inserda
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070954"
---
# <a name="pushed-tertiary-image-source"></a>Origen de imagen terciaria inserda

La función de botón PlayPauseStop requiere que defina la ubicación de la imagen presionada para el estado terciario del botón. Esta será la imagen que verán los usuarios cuando presionen el botón PlayPauseStop mientras transmiten una difusión en vivo.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superiores izquierdas (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen inserda para un origen de imagen terciaria, si la imagen está dentro del mapa de bits Pushed , escriba:


```C++
Pushed @ 324,0

```



Los estados terciarios no pueden tener una imagen deshabilitada. Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




