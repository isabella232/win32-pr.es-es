---
title: Recuperación de cambios
description: Una vez que un cliente se ha registrado para la notificación de determinados cambios y se produce uno o varios de estos cambios, el cliente recibe una notificación del administrador de tablas de enrutamiento.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea0de478a1f46e2281b18644026c2d8db44d113679f4f4f9bd5b18a1123e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788175"
---
# <a name="retrieving-changes"></a>Recuperación de cambios

Una vez que un cliente se ha registrado para la notificación de determinados cambios y se produce uno o varios de estos cambios, el cliente recibe una notificación del administrador de tablas de enrutamiento. El administrador de tablas de enrutamiento usa la devolución de llamada [**\_ RTM EVENT \_ CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) que se proporcionó en una llamada anterior a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity). El administrador de tablas de enrutamiento indica que se ha producido un evento \_ DE NOTIFICACIÓN DE CAMBIO DE RTM. \_

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Usar la devolución](use-the-event-notification-callback.md)de llamada de notificación de eventos .

 

 




