---
description: Consideraciones sobre los subprocesos
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Consideraciones sobre los subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467317"
---
# <a name="threading-considerations"></a>Consideraciones sobre los subprocesos

La grabadora de componentes en cola de COM+ es capaz de ejecutarse en el apartamento multiproceso (MTA) del proceso o en un apartamento de un solo subproceso (STA). Cuando la grabadora se ejecuta en sta, COM+ requiere que cada apartamento que contiene objetos tenga una cola de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) para controlar las llamadas de otros procesos y departamentos dentro del mismo proceso. Esto significa que la función de trabajo del subproceso debe tener un bucle de mensajes. Cuando se crea una instancia de un componente en cola, el puntero de interfaz devuelto siempre es un puntero de interfaz de proxy en lugar de un puntero de interfaz directa. El puntero es realmente una referencia a una instancia de la grabadora. Si esta referencia de interfaz de grabadora se pasa a otro subproceso, el subproceso original debe seguir ejecutando el bucle de mensajes Windows para que el subproceso receptor pueda desmarmarshal la interfaz. Si este no es el caso, el subproceso receptor se encuentra en una llamada a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Si usa primitivos para sincronizar los subprocesos, considere la posibilidad de usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) en lugar de otras funciones de sincronización. Esto comprueba si hay mensajes en la cola, así como el estado del objeto de sincronización.

 

 
