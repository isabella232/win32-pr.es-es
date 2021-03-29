---
title: Recuperando cambios
description: Una vez que un cliente se ha registrado para recibir notificaciones de determinados cambios y uno o varios de estos cambios se producen, el cliente recibe una notificación del administrador de tablas de enrutamiento.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532002"
---
# <a name="retrieving-changes"></a>Recuperando cambios

Una vez que un cliente se ha registrado para recibir notificaciones de determinados cambios y uno o varios de estos cambios se producen, el cliente recibe una notificación del administrador de tablas de enrutamiento. El administrador de tablas de enrutamiento utiliza la devolución de llamada de [**\_ \_ devolución**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) de llamada de evento de RTM que se proporcionó en una llamada anterior a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity). El administrador de tablas de enrutamiento indica que \_ se ha producido un evento de notificación de cambio de RTM \_ .

Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [usar la devolución de llamada de notificación de eventos](use-the-event-notification-callback.md).

 

 




