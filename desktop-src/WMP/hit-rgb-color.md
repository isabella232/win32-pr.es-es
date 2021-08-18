---
title: Color RGB de la pulsación
description: Color RGB de la pulsación
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Reproductor de Windows Media Máscaras móviles, colores de botón
- máscaras, colores de botón
- referencia de máscaras, botones
- botones en máscaras, colores
- referencia de color para máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c33e4b7eb2af9c1305a6644559e162c581c27b6b11e5b709376663082042d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390875"
---
# <a name="hit-rgb-color"></a>Color RGB de la pulsación

Si usa botones de región (PushHit, ToggleHit y 2PushHit), debe definir el color que Reproductor de Windows Media usará para determinar el área de pulsación del botón. Este valor debe especificarse mediante tres enteros positivos separados por comas. Estos enteros representan la cantidad de rojo, verde y azul para un color de mapa de bits y van de 0 a 255.

> [!Note]  
> Los tipos de botones están en desuso en las máscaras Reproductor de Windows Media 10 Mobile o posterior.

 

Puede usar cualquier color para los valores, pero asegúrese de que cada botón de región que defina tenga un color único en el archivo de imagen Región y que el valor de color que defina aquí como un número coincida con el color real usado en la imagen región.

En la tabla siguiente se muestran algunos colores típicos que puede usar.



| Valor       | Descripción |
|-------------|-------------|
| 0,0,0       | Negro       |
| 255,255,255 | Blanco       |
| 255,0,0     | Rojo         |
| 0,255,0     | Verde       |
| 0,0,255     | Azul        |



 

Si no usa botones de región, debe escribir lo siguiente:


```C++
0,0,0

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




