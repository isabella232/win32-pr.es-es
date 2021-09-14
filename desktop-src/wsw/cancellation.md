---
title: Cancelación
description: La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Cancelación de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359546"
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
| [**WsAbandoneCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandona una llamada, una llamada especificada en un proxy de servicio especificado.                                                        |



 

Para obtener información sobre las cancelaciones que afectan [a las operaciones](server-side-service-operations.md) de servicio del lado servidor y las devoluciones de llamada del modelo de servicio, vea [Cancelación de llamadas.](call-cancellation.md)


 

 




