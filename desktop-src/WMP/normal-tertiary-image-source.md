---
title: Origen de imagen terciario normal
description: Origen de imagen terciario normal
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418995"
---
# <a name="normal-tertiary-image-source"></a>Origen de imagen terciario normal

La función del botón PlayPauseStop requiere que defina la ubicación de la imagen normal para el estado terciario del botón. Será la imagen que verán los usuarios después de haber insertado el botón PlayPauseStop para empezar a transmitir una difusión en directo.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen normal para un origen de imagen terciario, si la imagen está dentro del mapa de bits insertado, escriba:


```C++
Pushed @ 286,0

```



Los Estados terciarios no pueden tener una imagen deshabilitada. Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




