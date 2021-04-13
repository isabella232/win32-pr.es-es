---
title: Trabajar con el reproductor
description: Trabajar con el reproductor
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Máscaras de Windows Media Player, atributo Player en JScript
- máscaras, atributo Player en JScript
- atributos, reproductor
- atributo Player
- Archivos JScript para máscaras, atributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419150"
---
# <a name="working-with-the-player"></a>Trabajar con el reproductor

Al usar Microsoft JScript para tener acceso a los métodos y las propiedades de Windows Media Player, debe usar el nombre "Player" como nombre del control. Por ejemplo, para hacer referencia al método STOP, debe escribir:


```C++
player.Controls.Stop()

```



El atributo global **Player** es la clave para tener acceso al control de Media Player de Windows a través de scripting de máscara. A través de este atributo, se puede tener acceso a todos los objetos del control de Media Player de Windows para modificarlos en tiempo de ejecución a través de sus propiedades y métodos. Además, el elemento **Player** está disponible para que pueda especificar controladores de eventos y el atributo **URL** en tiempo de diseño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar JScript**](using-jscript.md)
</dt> </dl>

 

 




