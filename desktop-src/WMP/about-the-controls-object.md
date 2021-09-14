---
title: Acerca del objeto Controls
description: Acerca del objeto Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Reproductor de Windows Media,Controls (objeto)
- Reproductor de Windows Media modelo de objetos, objeto Controls
- object model,Controls (objeto)
- Reproductor de Windows Media ActiveX control, objeto Controls
- ActiveX control, objeto Controls
- Reproductor de Windows Media Control de ActiveX móvil, objeto Controls
- Reproductor de Windows Media Mobile,Controls (objeto)
- Objeto Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264783"
---
# <a name="about-the-controls-object"></a>Acerca del objeto Controls

El **objeto Controls** rige el transporte de contenido multimedia digital a través del control mediante métodos como **Play** y **Stop.** Solo se accede a él a través de **la propiedad Controls** del objeto **Player.** La **propiedad Controls** devuelve el objeto **Controls.** Solo puede acceder a las propiedades del **objeto Controls** después de crearlo. Por ejemplo, para usar el **método Play,** debe usar el código siguiente:


```C++
player.controls.play();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




