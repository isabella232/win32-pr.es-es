---
title: Reproducción y posicionamiento
description: Reproducción y posicionamiento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161383"
---
# <a name="playback-and-positioning"></a>Reproducción y posicionamiento

Varios comandos MCI, como [**play**](play.md) [**(MCI \_ PLAY),**](mci-play.md) [**stop**](stop.md) [**(MCI \_ STOP),**](mci-stop.md) [**pause**](pause.md) [**(MCI \_ PAUSE),**](mci-pause.md) [**resume**](resume.md) [**(MCI \_ RESUME)**](mci-resume.md)y [**seek**](seek.md) [**(MCI \_ SEEK),**](mci-seek.md)afectan a la reproducción o posicionamiento de un archivo multimedia. Si un dispositivo MCI recibe un comando de reproducción mientras hay otro comando de reproducción en curso, acepta el comando y detiene o reemplaza el comando anterior.

Muchos comandos MCI, como [**set**](set.md) [**(MCI \_ SET),**](mci-set.md)no afectan a la reproducción. Una notificación de uno de estos comandos no interfiere con los comandos de reproducción o posición pendientes, siempre y cuando las notificaciones no se realicen desde la misma instancia del controlador. Por ejemplo, puede emitir un comando **set** o [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) mientras un dispositivo realiza un comando **seek** sin detener o supersedar el **comando seek.**

Sin embargo, solo puede haber una notificación pendiente. Por ejemplo, si una aplicación  solicita una notificación de reproducción y sigue esa  solicitud con el estado **"start** position notify", la notificación de reproducción devolverá "sustituido" y la notificación del comando de estado devolverá cuando haya finalizado. En este caso, sin embargo, el **comando play** seguirá teniendo éxito, aunque la aplicación no haya recibido la notificación.

 

 




