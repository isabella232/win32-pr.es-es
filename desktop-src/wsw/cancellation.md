---
title: Cancelación
description: La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Cancelación de servicios web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841785"
---
# <a name="cancellation"></a>Cancelación

La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.

La función que use para cancelar una operación depende del objeto afectado.

| Función                                           | Descripción                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Cancela todas las entradas y salidas pendientes en un canal especificado y establece el estado del canal en WS \_ CHANNEL \_ STATE \_ FAULTED. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Cancela todas las entradas y salidas pendientes en un agente de escucha especificado.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrumpe e interrumpe las operaciones actuales en el host de servicio.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandona una llamada, una llamada especificada en un proxy de servicio especificado.                                                        |



 

Para obtener información sobre las cancelaciones que afectan a [las operaciones de servicio del](server-side-service-operations.md) lado servidor y a las devoluciones de llamada del modelo de servicio, vea [Cancelación de llamadas.](call-cancellation.md)


 

 




