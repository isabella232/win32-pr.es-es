---
title: Marca de espera
description: Marca de espera
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076380"
---
# <a name="the-wait-flag"></a>Marca de espera

Los comandos MCI normalmente vuelven al usuario inmediatamente, incluso si tardan varios minutos en completar la acción iniciada por el comando. Puede usar la marca "Wait" ( \_ espera de MCI) para indicar al dispositivo que espere hasta que se complete la acción solicitada antes de devolver el control a la aplicación.

Por ejemplo, el siguiente comando [**Play**](play.md) no devolverá el control a la aplicación hasta que se complete la reproducción:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> El usuario puede cancelar una operación de espera presionando una tecla de salto. De forma predeterminada, esta tecla es CTRL + INTER. Las aplicaciones pueden volver a definir esta clave mediante el comando [**break**](break.md) (el [**\_ interruptor de MCI**](mci-break.md)). (**El \_ salto de MCI** usa la estructura de [**parms de \_ interrupción \_ de MCI**](mci-break-parms.md) ). Cuando se cancela una operación de espera, MCI intenta devolver el control a la aplicación sin interrumpir el comando asociado a la marca "Wait".

 

 

 




