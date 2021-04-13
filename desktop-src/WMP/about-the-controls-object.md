---
title: Acerca del objeto Controls
description: Acerca del objeto Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player, Controls (objeto)
- Modelo de objetos de Windows Media Player, objetos Controls
- modelo de objetos, controles (objeto)
- Control ActiveX de Windows Media Player, controles (objeto)
- Control ActiveX, controles (objeto)
- Control ActiveX móvil de Windows Media Player, controles (objeto)
- Windows Media Player Mobile, objetos Controls
- Controls (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418382"
---
# <a name="about-the-controls-object"></a>Acerca del objeto Controls

El objeto **Controls** rige el transporte de contenido multimedia digital a través del control mediante métodos como **Play** y **Stop**. Solo se tiene acceso a ella a través de la propiedad **Controls** del objeto **Player** . La propiedad **Controls** devuelve el objeto **Controls** . Solo se puede tener acceso a las propiedades del objeto **Controls** una vez creado. Por ejemplo, para usar el método **Play** , debe usar el código siguiente:


```C++
player.controls.play();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




