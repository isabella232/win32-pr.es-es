---
description: Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Crear una rutina de devolución de llamada de cola personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0602e32ef97ea962ca91375318bb563c0809da0dc4877aa6c9439644b52408e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887516"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Crear una rutina de devolución de llamada de cola personalizada

Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada. Esta función debe tener el mismo formato que [*FileCallback.*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a) Esto es útil si necesita una rutina de devolución de llamada para controlar una notificación de una manera diferente a la proporcionada por la rutina de devolución de llamada de cola predeterminada.

Si solo es necesario cambiar una pequeña parte del comportamiento de la rutina de devolución de llamada de cola predeterminada, puede crear una rutina de devolución de llamada personalizada para filtrar las notificaciones, controlar solo aquellas que requieren un comportamiento especial y llamar a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para las demás.

Por ejemplo, si desea controlar los errores de eliminación de archivos personalizados, podría crear una función de devolución de llamada personalizada, *MyCallback*. Esta función interceptaría y procesaría las notificaciones [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) y llamaría a la función de devolución de llamada de cola predeterminada para todas las demás notificaciones. *MyCallback* devuelve un valor para las notificaciones de error de eliminación. Para todas las demás notificaciones, *MyCallback* pasa cualquier valor que la rutina de devolución de llamada de cola predeterminada haya devuelto a la cola.

Este flujo de control se muestra en el diagrama siguiente.

![flechas y cuadros que muestran el flujo de datos para la función de devolución de llamada personalizada](images/callback.png)

> [!IMPORTANT]
> Si la función de devolución de llamada personalizada llama a la rutina de devolución de llamada de cola predeterminada, debe pasar el puntero void devuelto por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) a la rutina de devolución de llamada predeterminada.

 

 

 
