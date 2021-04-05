---
title: Cancelación
description: La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Servicios Web de cancelación para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359545"
---
# <a name="cancellation"></a>Cancelación

La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.

La función que se usa para cancelar una operación depende del objeto afectado.

| Función                                           | Descripción                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Cancela todas las entradas y salidas pendientes en un canal especificado y establece el estado del canal en estado de canal de WS con \_ \_ \_ errores. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Cancela todas las entradas y salidas pendientes en un agente de escucha especificado.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrumpe y suspende las operaciones actuales en el host de servicio.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandona una llamada a, una llamada especificada en un proxy de servicio especificado.                                                        |



 

Para obtener información sobre las cancelaciones que afectan a [las operaciones de servicio del lado servidor y las](server-side-service-operations.md) devoluciones de llamada del modelo de servicio, consulte [cancelación de llamadas](call-cancellation.md).


 

 




