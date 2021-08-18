---
description: El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control de servicios.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servicios multiproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003733"
---
# <a name="multithreaded-services"></a>Servicios multiproceso

El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control del servicio. El servicio debe responder a los eventos de control de forma oportuna para que el SCM pueda realizar un seguimiento del estado del servicio. Además, el estado del servicio debe coincidir con la descripción de su estado que recibe el SCM.

Debido a este mecanismo de comunicación entre un servicio y el SCM, debe tener cuidado al usar varios subprocesos en un servicio. Cuando el SCM indica a un servicio que se detenga, debe esperar a que todos los subprocesos se cierren antes de informar al SCM de que el servicio está detenido. De lo contrario, el SCM puede confundirse con el estado del servicio y podría no cerrarse correctamente.

Es necesario notificar al SCM que el servicio responde al evento de control de detención y que se está avanzando en la detención del servicio. El SCM supondrá que el servicio está progresando si el servicio responde (a través de [**SetServiceStatus)**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)dentro del tiempo (sugerencia de espera) especificado en la llamada anterior a **SetServiceStatus** y el punto de comprobación se actualiza para que sea mayor que el punto de control especificado en la llamada anterior a **SetServiceStatus**.

Si el servicio informa al SCM de que el servicio se ha detenido antes de que todos los subprocesos se cierren, es posible que el SCM interprete esto como un desenlaz. Esto podría dar lugar a un estado en el que el servicio no se puede detener ni reiniciar.

 

 



