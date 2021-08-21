---
description: Consideraciones sobre los subprocesos
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Consideraciones sobre los subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac13cdfcc398f6a7c23eef26011ed1ee6e26eb138570d225c8bd108a4a30318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812156"
---
# <a name="threading-considerations"></a>Consideraciones sobre los subprocesos

La grabadora de componentes en cola com+ es capaz de ejecutarse en el apartamento multiproceso (MTA) del proceso o en un apartamento de un solo subproceso (STA). Cuando la grabadora se ejecuta en el STA, COM+ requiere que cada apartamento que contiene objetos tenga una cola de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) para controlar las llamadas de otros procesos y departamentos dentro del mismo proceso. Esto significa que la función de trabajo del subproceso debe tener un bucle de mensajes. Cuando se crea una instancia de un componente en cola, el puntero de interfaz devuelto siempre es un puntero de interfaz de proxy en lugar de un puntero de interfaz directa. El puntero es realmente una referencia a una instancia de la grabadora. Si esta referencia de interfaz de grabadora se pasa a otro subproceso, el subproceso original debe seguir ejecutando el bucle de mensajes Windows para que el subproceso receptor pueda desmarshal la interfaz. Si este no es el caso, el subproceso receptor se encuentra en una llamada a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Si usa primitivas para sincronizar los subprocesos, considere la posibilidad de usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) en lugar de otras funciones de sincronización. Esto comprueba los mensajes de la cola, así como el estado del objeto de sincronización.

 

 
