---
description: Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de cola, el contexto para ella debe inicializarse mediante las funciones SetupInitDefaultQueueCallback o SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmación de la cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887526"
---
# <a name="committing-the-queue"></a>Confirmación de la cola

Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de cola, el contexto para ella debe inicializarse mediante las funciones [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) Si usa una función de devolución de llamada personalizada que nunca llama a la función de devolución de llamada predeterminada, este paso no es necesario.

Una vez creada la cola y inicializada la función de devolución de llamada que procesará las notificaciones de cola, puede llamar a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar las operaciones que se han puesto en cola.

En el ejemplo siguiente se [**usa SetupCommitFileQueue para**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirmar la cola mediante la rutina de devolución de llamada predeterminada.

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

En el ejemplo anterior, MyQueue es la cola que se va a confirmar, OwnerWindow es la ventana que poseerá los cuadros de diálogo creados por la rutina de devolución de llamada predeterminada, SetupDefaultQueueCallback especifica que se usará la función de devolución de llamada predeterminada y *Context* es un puntero a la estructura devuelta por la llamada anterior a [**SetupInitDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)

 

 



