---
description: Si se inicializa la rutina de devolución de llamada de cola predeterminada y se especifica cuando se llama a SetupCommitFileQueue, la cola llama a la rutina de devolución de llamada de cola predeterminada internamente y necesita hacer nada más.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Llamar a la rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669794"
---
# <a name="calling-the-default-queue-callback-routine"></a>Llamar a la rutina de devolución de llamada de cola predeterminada

Si se inicializa la rutina de devolución de llamada de cola predeterminada y se especifica cuando se llama a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , la cola llama a la rutina de devolución de llamada de cola predeterminada internamente y necesita hacer nada más.

Si crea una rutina de devolución de llamada de filtro que se basa en la rutina de devolución de llamada de cola predeterminada para controlar un subconjunto de las notificaciones de cola, la rutina de devolución de llamada del filtro debe llamar explícitamente a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

> [!IMPORTANT]
> Cuando llame a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explícitamente, debe pasar el puntero void devuelto por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

> [!Note]  
> Una manera de hacerlo es crear una estructura de contexto para la rutina de devolución de llamada personalizada que incluya como uno de sus miembros el puntero void devuelto por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

 

 



