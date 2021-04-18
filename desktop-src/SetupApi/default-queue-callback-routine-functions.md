---
description: Las siguientes funciones se usan con la rutina de devolución de llamada de cola predeterminada.
ms.assetid: 2122c1cf-3ea9-4601-8a2e-dd991b09edc2
title: Funciones de rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98be595ac82f319ac2718f8ec1fc4fd00bea1ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667883"
---
# <a name="default-queue-callback-routine-functions"></a>Funciones de rutina de devolución de llamada de cola predeterminada

Las siguientes funciones se usan con la rutina de devolución de llamada de cola predeterminada.



| Función                                                                   | Descripción                                                                                                                                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)             | La rutina de devolución de llamada de cola predeterminada.                                                                                                                                                    |
| [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)     | Inicializa la información de contexto que necesita la rutina de devolución de llamada de cola predeterminada.                                                                                                          |
| [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) | Inicializa la información de contexto que necesita la rutina de devolución de llamada de cola predeterminada y especifica una ventana alternativa para mostrar los mensajes de progreso.                                           |
| [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback)     | Libera los recursos asignados por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) y [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). |



 

 

 



