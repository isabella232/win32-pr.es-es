---
title: Golpear color RGB
description: Golpear color RGB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Máscaras móviles de Windows Media Player, colores de botón
- máscaras, colores de botón
- referencia de las máscaras, botones
- botones en máscaras, colores
- referencia de color para máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695422"
---
# <a name="hit-rgb-color"></a>Golpear color RGB

Si utiliza los botones de región (PushHit, ToggleHit y 2PushHit), debe definir el color que usará Windows Media Player para determinar el área de aciertos del botón. Este valor debe especificarse mediante tres enteros positivos separados por comas. Estos enteros representan la cantidad de rojo, verde y azul para un color de mapa de bits y oscilan entre 0 y 255.

> [!Note]  
> Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.

 

Puede usar los colores de los valores, pero asegúrese de que cada botón de la región que defina tenga un color único en el archivo de imagen de región y que el valor de color que defina aquí como un número coincida con el color real utilizado en la imagen de la región.

En la tabla siguiente se muestran algunos colores típicos que podría querer usar.



| Value       | Descripción |
|-------------|-------------|
| 0, 0, 0       | Negro       |
| 255.255.255 | Blanco       |
| 255, 0, 0     | Rojo         |
| 0255, 0     | Verde       |
| 0, 0255     | Azul        |



 

Si no utiliza botones de región, debe escribir lo siguiente:


```C++
0,0,0

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




