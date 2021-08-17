---
title: Creación de un receptor de notificaciones
description: Creación de un receptor de notificaciones
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480097"
---
# <a name="creating-a-notification-sink"></a>Creación de un receptor de notificaciones

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para que Microsoft Agent notifique los eventos, debe implementar la interfaz [**IAgentNotifySink**](events.md)o [**IAgentNotifySinkEx,**](iagentnotifysinkex.md) y crear y registrar un objeto de ese tipo siguiendo las convenciones COM:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Recuerde anular el registro del receptor de notificaciones cuando la aplicación se cierre y libere las interfaces de Microsoft Agent.

 

 




