---
description: Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Crear una rutina de devolución de llamada de cola personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911558"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Crear una rutina de devolución de llamada de cola personalizada

Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada. Esta función debe tener el mismo formato que [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Esto resulta útil si necesita una rutina de devolución de llamada para controlar una notificación de una manera distinta de la que proporciona la rutina de devolución de llamada de cola predeterminada.

Si solo es necesario cambiar una pequeña parte del comportamiento de la rutina de devolución de llamada de cola predeterminada, puede crear una rutina de devolución de llamada personalizada para filtrar las notificaciones, controlar solo aquellas que requieren un comportamiento especial y llamar a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para los demás.

Por ejemplo, si deseara personalizar el control de errores de eliminación de archivos, podría crear una función de devolución de llamada personalizada, *DoCallBack*. Esta función interceptará y procesará las notificaciones de [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) y llamará a la función de devolución de llamada de cola predeterminada para todas las demás notificaciones. *DoCallBack* devuelve un valor para las notificaciones de error de eliminación. Para todas las demás notificaciones, la *devolución de llamada* pasa cualquier valor que la rutina de devolución de llamada de cola predeterminada devuelva a la cola.

Este flujo de control se muestra en el diagrama siguiente.

![flechas y cuadros que muestran el flujo de datos para la función de devolución de llamada personalizada](images/callback.png)

> [!IMPORTANT]
> Si la función de devolución de llamada personalizada llama a la rutina de devolución de llamada de cola predeterminada, debe pasar el puntero void devuelto por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) a la rutina de devolución de llamada predeterminada.

 

 

 
