---
title: Proxy de servicio y sesiones
description: El proxy de servicio tiene comportamientos especiales para enlaces de canal de sesión y no basados en sesión.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Servicios web de sesiones y proxy de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360570"
---
# <a name="service-proxy-and-sessions"></a>Proxy de servicio y sesiones

El [proxy de servicio](service-proxy.md) tiene comportamientos especiales para enlaces de canal de sesión y no basados en sesión. El proxy de servicio proporciona semántica basada en sesión si el enlace de canal subyacente se basa en la sesión. En este caso, se usa un único canal para dar servicio a las llamadas. Sin embargo, si el enlace de canal no está basado en sesión, el proxy de servicio crea un canal independiente para cada llamada. Sin embargo, tenga en cuenta que los canales no basados en sesión se agrupan y quizás se reutilizan. Al volver a usar un canal, el proxy de servicio mantiene el canal abierto si el canal subyacente no ha dado error o la llamada a un canal ha dado lugar a un error del proxy de servicio en el canal. Tenga en cuenta que. excepto en caso de error, una vez abierto un canal, se mantiene abierto mientras el proxy de servicio esté abierto y solo se cierre cuando se cierre el proxy de servicio.


Si el enlace de canal se basa en la sesión y el canal subyacente falla, la máquina de estado del proxy de servicio pasará al estado DE ERROR DEL PROXY DE SERVICIO de [**WS. \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) En el caso del enlace de canal no basado en sesión, un error en el canal subyacente no hace que el proxy haga la transición al estado DE ERROR DE ESTADO DE PROXY DE SERVICIO de **WS. \_ \_ \_ \_**

Para obtener más información sobre el proxy de servicio y su relación con el estado, vea el tema [Proxy de](service-proxy.md) servicio. Para obtener ejemplos de diferentes enlaces de canal, vea los ejemplos siguientes:

-   enlace de canal que no es de sesión, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   enlace de canal basado en sesión, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




