---
description: Antes de que se pueda usar la rutina de devolución de llamada de cola predeterminada, ya sea mediante la especificación de la rutina de devolución de llamada al confirmar una cola de archivos o mediante una llamada a ella desde una rutina de devolución de llamada personalizada, debe inicializarse.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Inicialización y finalización del contexto de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667995"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Inicialización y finalización del contexto de devolución de llamada

Antes de que se pueda usar la rutina de devolución de llamada de cola predeterminada, ya sea mediante la especificación de la rutina de devolución de llamada al confirmar una cola de archivos o mediante una llamada a ella desde una rutina de devolución de llamada personalizada, debe inicializarse.

La función [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) crea la estructura de contexto usada por la rutina de devolución de llamada de cola predeterminada. Devuelve un puntero void a esa estructura. Esta estructura es esencial para la operación de la rutina de devolución de llamada predeterminada y se debe pasar a la rutina de devolución de llamada. Puede hacerlo especificando el puntero void como el contexto en una llamada a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)o especificando el puntero void como parámetro de contexto al llamar a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) desde una rutina de devolución de llamada personalizada. La aplicación de instalación no debe modificar ni hacer referencia a esta estructura de contexto.

La función [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) también Inicializa un contexto para la rutina de devolución de llamada de cola predeterminada, pero especifica una segunda ventana para recibir un mensaje de progreso especificado por el llamador cada vez que la cola envía una notificación. Esto le permite usar los cuadros de diálogo de error y de solicitud de disco predeterminados, así como insertar una barra de progreso en una segunda ventana, por ejemplo, en una página de un asistente para la instalación.

Independientemente de si ha inicializado el contexto utilizado por la rutina de devolución de llamada de cola predeterminada con [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), una vez que las operaciones en cola hayan terminado de procesarse, llame a [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) para liberar los recursos asignados al inicializar la estructura de contexto.

 

 



