---
title: Origen de la imagen terciaria insertada
description: Origen de la imagen terciaria insertada
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994253"
---
# <a name="pushed-tertiary-image-source"></a>Origen de la imagen terciaria insertada

La función del botón PlayPauseStop requiere que defina la ubicación de la imagen insertada para el estado terciario del botón. Será la imagen que verán los usuarios cuando inserten el botón PlayPauseStop durante el streaming de una difusión en directo.

Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio. A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.

Por ejemplo, para definir la imagen insertada para un origen de imagen terciario, si la imagen está dentro del mapa de bits insertado, escriba:


```C++
Pushed @ 324,0

```



Los Estados terciarios no pueden tener una imagen deshabilitada. Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




