---
title: Acerca de los objetos Error y ErrorItem
description: Acerca de los objetos Error y ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Reproductor de Windows Media,Error (objeto)
- Reproductor de Windows Media modelo de objetos, objeto Error
- object model,Error (objeto)
- Reproductor de Windows Media ActiveX control, objeto Error
- ActiveX control, objeto Error
- Reproductor de Windows Media Control de ActiveX móvil, objeto Error
- Reproductor de Windows Media Mobile,Error (objeto)
- Objeto de error
- Reproductor de Windows Media, objeto ErrorItem
- Reproductor de Windows Media modelo de objetos, objeto ErrorItem
- object model,ErrorItem object
- Reproductor de Windows Media ActiveX control, objeto ErrorItem
- ActiveX control, objeto ErrorItem
- Reproductor de Windows Media Control ActiveX móvil, objeto ErrorItem
- Reproductor de Windows Media Mobile,ErrorItem, objeto
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264759"
---
# <a name="about-the-error-and-erroritem-objects"></a>Acerca de los objetos Error y ErrorItem

Los **objetos Error** y **ErrorItem** rigen las funcionalidades de control de errores de Reproductor de Windows Media. El **objeto Error** se obtiene del objeto **Player** a través de la propiedad **de error.** Puede obtener un código específico del objeto **Error** mediante la propiedad **item** del **objeto Error** para crear el **objeto ErrorItem.** Por ejemplo, para obtener el código de error del primer elemento de error, escriba:


```C++
myerrorcode = player.error.item(0).errorCode;

```



También puede invocar la Ayuda web con el **objeto Error** mediante el código siguiente:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




