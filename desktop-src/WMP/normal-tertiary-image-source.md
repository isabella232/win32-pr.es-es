---
title: Origen de la imagen terciaria normal
description: Origen de la imagen terciaria normal
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967395"
---
# <a name="normal-tertiary-image-source"></a>Origen de la imagen terciaria normal

La función de botón PlayPauseStop requiere que defina la ubicación de la imagen normal para el estado terciario del botón. Esta será la imagen que verán los usuarios después de haber presionado el botón PlayPauseStop para empezar a transmitir una difusión en vivo.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio, el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superiores izquierdas (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen normal para un origen de imagen terciaria, si la imagen está dentro del mapa de bits Pushed , escriba:


```C++
Pushed @ 286,0

```



Los estados terciarios no pueden tener una imagen deshabilitada. Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




