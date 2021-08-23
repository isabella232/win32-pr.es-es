---
title: Trabajar con el reproductor
description: Trabajar con el reproductor
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Reproductor de Windows Media máscaras, atributo player en JScript
- skins,player attribute in JScript
- attributes,player
- atributo player
- JScript para máscaras, atributo player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77098f161244488d5097d2d022f105628a43ba50a40218da01295d99f2de0cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566987"
---
# <a name="working-with-the-player"></a>Trabajar con el reproductor

Al usar Microsoft JScript para acceder a métodos y propiedades de Reproductor de Windows Media, debe usar el nombre "player" como nombre del control. Por ejemplo, para hacer referencia al método Stop, debe escribir:


```C++
player.Controls.Stop()

```



El **atributo** global del reproductor es la clave para acceder al control Reproductor de Windows Media mediante scripting de máscara. A través de este atributo, todos los objetos del control Reproductor de Windows Media pueden ser accesibles para la modificación en tiempo de ejecución a través de sus propiedades y métodos. Además, el elemento **PLAYER** está disponible para que pueda especificar controladores de eventos y el atributo **url** en tiempo de diseño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de JScript**](using-jscript.md)
</dt> </dl>

 

 




