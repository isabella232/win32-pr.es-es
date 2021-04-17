---
description: Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de la cola, el contexto para ella se debe inicializar mediante las funciones SetupInitDefaultQueueCallback o SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmar la cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667611"
---
# <a name="committing-the-queue"></a>Confirmar la cola

Si se va a llamar a la función de devolución de llamada predeterminada durante el compromiso de la cola, el contexto para ella se debe inicializar mediante las funciones [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) . Si usa una función de devolución de llamada personalizada que nunca llama a la función de devolución de llamada predeterminada, este paso no es necesario.

Una vez que se ha generado la cola y se ha inicializado la función de devolución de llamada que procesará las notificaciones de cola, puede llamar a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar las operaciones que se han puesto en cola.

En el ejemplo siguiente se usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar la cola mediante la rutina de devolución de llamada predeterminada.

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

En el ejemplo anterior, alqueue es la cola que se va a confirmar, OwnerWindow es la ventana que será propietaria de los cuadros de diálogo creados por la rutina de devolución de llamada predeterminada, SetupDefaultQueueCallback especifica que se utilizará la función de devolución de llamada predeterminada y *Context* es un puntero a la estructura devuelta por la llamada anterior a [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



