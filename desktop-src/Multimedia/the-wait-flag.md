---
title: La marca wait
description: La marca wait
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801439"
---
# <a name="the-wait-flag"></a>La marca wait

Los comandos de MCI normalmente vuelven al usuario inmediatamente, incluso si se tardan varios minutos en completar la acción iniciada por el comando. Puede usar la marca "wait" (MCI WAIT) para dirigir el dispositivo a esperar hasta que se complete la acción solicitada antes de devolver \_ el control a la aplicación.

Por ejemplo, el siguiente [**comando play**](play.md) no devolverá el control a la aplicación hasta que se complete la reproducción:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> El usuario puede cancelar una operación de espera presionando una tecla de interrupción. De forma predeterminada, esta tecla es CTRL+BREAK. Las aplicaciones pueden volver a definir esta clave mediante [**el comando break**](break.md) ([**MCI \_ BREAK**](mci-break.md)). (**MCI \_ BREAK usa** la estructura [**\_ MCI BREAK \_ PARMS).**](mci-break-parms.md) Cuando se cancela una operación de espera, MCI intenta devolver el control a la aplicación sin interrumpir el comando asociado a la marca "wait".

 

 

 




