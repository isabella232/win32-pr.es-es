---
description: Consideraciones sobre los subprocesos
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Consideraciones sobre los subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080286"
---
# <a name="threading-considerations"></a>Consideraciones sobre los subprocesos

La grabadora de componentes en cola de COM+ es capaz de ejecutarse en el contenedor multiproceso (MTA) del proceso o en un contenedor uniproceso (STA). Cuando la grabadora se ejecuta en el STA, COM+ requiere que cada apartamento que contenga los objetos deba tener una cola de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) para controlar las llamadas desde otros procesos y apartamentos dentro del mismo proceso. Esto significa que la función de trabajo del subproceso debe tener un bucle de mensajes. Cuando se crea una instancia de un componente en cola, el puntero de interfaz devuelto es siempre un puntero de interfaz de proxy en lugar de un puntero de interfaz directo. El puntero es realmente una referencia a una instancia de la grabadora. Si esta referencia de la interfaz de la grabadora se pasa a otro subproceso, el subproceso original todavía debe ejecutar el bucle de mensajes de Windows para que el subproceso receptor pueda quitar las referencias de la interfaz. Si no es así, el subproceso receptor se bloquea en una llamada a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Si usa primitivas para sincronizar los subprocesos, considere la posibilidad de usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) en lugar de otras funciones de sincronización. Comprueba si hay mensajes en la cola, así como el estado del objeto de sincronización.

 

 
