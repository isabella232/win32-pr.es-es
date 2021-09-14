---
title: Marca de espera
description: Marca de espera
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260679"
---
# <a name="the-wait-flag"></a>Marca de espera

Los comandos de MCI normalmente vuelven al usuario inmediatamente, aunque tarde varios minutos en completar la acción iniciada por el comando. Puede usar la marca "wait" (MCI WAIT) para dirigir el dispositivo a esperar hasta que se complete la acción solicitada antes de devolver \_ el control a la aplicación.

Por ejemplo, el siguiente [**comando de**](play.md) reproducción no devolverá el control a la aplicación hasta que se complete la reproducción:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> El usuario puede cancelar una operación de espera presionando una tecla de interrupción. De forma predeterminada, esta tecla es CTRL+BREAK. Las aplicaciones pueden volver a definir esta clave mediante [**el comando break**](break.md) ([**MCI \_ BREAK**](mci-break.md)). **(MCI \_ BREAK usa** la estructura [**\_ MCI BREAK \_ PARMS).**](mci-break-parms.md) Cuando se cancela una operación de espera, MCI intenta devolver el control a la aplicación sin interrumpir el comando asociado a la marca "wait".

 

 

 




