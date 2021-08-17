---
description: Antes de que se pueda usar la rutina de devolución de llamada de cola predeterminada, ya sea especificándose como rutina de devolución de llamada al confirmar una cola de archivos o llamándose desde una rutina de devolución de llamada personalizada, se debe inicializar.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Inicialización y terminación del contexto de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67df0707f91a17369503fa17ecbeefef3eb6827be60285b0b778b07d98eba3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965438"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Inicialización y terminación del contexto de devolución de llamada

Antes de que se pueda usar la rutina de devolución de llamada de cola predeterminada, ya sea especificándose como rutina de devolución de llamada al confirmar una cola de archivos o llamándose desde una rutina de devolución de llamada personalizada, se debe inicializar.

La [**función SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) compila la estructura de contexto que usa la rutina de devolución de llamada de cola predeterminada. Devuelve un puntero void a esa estructura. Esta estructura es esencial para la operación de la rutina de devolución de llamada predeterminada y debe pasarse a la rutina de devolución de llamada. Puede hacerlo especificando el puntero void como contexto en una llamada a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)o especificando el puntero void como parámetro de contexto al llamar a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) desde una rutina de devolución de llamada personalizada. La aplicación de instalación no debe modificar ni hacer referencia a esta estructura de contexto.

La función [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) también inicializa un contexto para la rutina de devolución de llamada de cola predeterminada, pero especifica una segunda ventana para recibir un mensaje de progreso especificado por el autor de la llamada cada vez que la cola envía una notificación. Esto le permite usar los cuadros de diálogo de error y aviso de disco predeterminados, así como insertar también una barra de progreso en una segunda ventana, por ejemplo, en una página de un Asistente para instalación.

Independientemente de si ha inicializado el contexto usado por la rutina de devolución de llamada de cola predeterminada con [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), una vez que las operaciones en cola han finalizado el procesamiento, llame a [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) para liberar los recursos asignados al inicializar la estructura de contexto.

 

 



