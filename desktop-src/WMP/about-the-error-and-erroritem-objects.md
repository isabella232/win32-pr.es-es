---
title: Acerca de los objetos error y ErrorItem
description: Acerca de los objetos error y ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Media Player de Windows, objeto error
- Modelo de objetos de Windows Media Player, objeto error
- modelo de objetos, error (objeto)
- Control ActiveX de Windows Media Player, objeto error
- Control ActiveX, error (objeto)
- Control ActiveX móvil de Windows Media Player, objeto error
- Windows Media Player Mobile, error (objeto)
- Objeto de error
- Media Player de Windows, objeto ErrorItem
- Modelo de objetos de Media Player de Windows, objeto ErrorItem
- modelo de objetos, ErrorItem (objeto)
- Control ActiveX de Windows Media Player, objeto ErrorItem
- Control ActiveX, objeto ErrorItem
- Control ActiveX de Windows Media Player Mobile, objeto ErrorItem
- Windows Media Player Mobile, objeto ErrorItem
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357213"
---
# <a name="about-the-error-and-erroritem-objects"></a>Acerca de los objetos error y ErrorItem

Los objetos **error** y **ErrorItem** rigen las capacidades de control de errores de Windows Media Player. El objeto de **error** se obtiene del objeto **Player** a través de la propiedad **error** . Puede obtener un código específico del objeto de **error** mediante la propiedad **Item** del objeto **error** para crear el objeto **ErrorItem** . Por ejemplo, para obtener el código de error del primer elemento de error, escriba:


```C++
myerrorcode = player.error.item(0).errorCode;

```



También puede invocar la ayuda web con el objeto de **error** mediante el código siguiente:


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

 

 




