---
description: El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control de servicios.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servicios multiproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668294"
---
# <a name="multithreaded-services"></a>Servicios multiproceso

El administrador de control de servicios (SCM) controla un servicio mediante el envío de eventos de control de servicio a la rutina del controlador de control del servicio. El servicio debe responder a los eventos de control de forma oportuna para que el SCM pueda realizar un seguimiento del estado del servicio. Además, el estado del servicio debe coincidir con la descripción de su estado que recibe el SCM.

Debido a este mecanismo de comunicación entre un servicio y el SCM, debe tener cuidado al usar varios subprocesos en un servicio. Cuando se indica a un servicio que lo detenga el SCM, debe esperar a que finalicen todos los subprocesos antes de informar al SCM de que el servicio se ha detenido. De lo contrario, el SCM puede confundirse con respecto al estado del servicio y podría no cerrarse correctamente.

El SCM debe recibir una notificación de que el servicio responde al evento STOP control y que se está realizando el progreso al detener el servicio. El SCM asumirá que el servicio progresa si el servicio responde (a la [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) dentro del tiempo (sugerencia de espera) especificado en la llamada anterior a **SetServiceStatus** y el punto de comprobación se actualiza para que sea mayor que el punto de control especificado en la llamada anterior a **SetServiceStatus**.

Si el servicio informa al SCM de que el servicio se ha detenido antes de que todos los subprocesos se hayan cerrado, es posible que el SCM lo interprete como contradicción. Esto podría dar lugar a un estado en el que el servicio no se puede detener o reiniciar.

 

 



