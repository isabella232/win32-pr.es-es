---
title: Proxy de servicio y sesiones
description: El proxy de servicio tiene comportamientos especiales para los enlaces de canal de sesión y no basados en sesión.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Servicios Web de proxy de servicio y sesiones para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078623"
---
# <a name="service-proxy-and-sessions"></a>Proxy de servicio y sesiones

El [proxy de servicio](service-proxy.md) tiene comportamientos especiales para los enlaces de canal de sesión y no basados en sesión. El proxy de servicio proporciona semántica basada en sesión si el enlace de canal subyacente está basado en sesión. En este caso, se utiliza un canal único para atender las llamadas. Sin embargo, si el enlace de canal no está basado en sesión, el proxy de servicio crea un canal independiente para cada llamada. Sin embargo, tenga en cuenta que los canales no basados en sesión se agrupan y quizás se reutilizan. En la reutilización de un canal, el proxy de servicio mantiene el canal abierto si el canal subyacente no ha generado un error o la llamada en un canal ha dado lugar a un error en el canal del proxy de servicio. Tenga en cuenta que. excepto en el caso de que se produzca un error, cuando se abre un canal se mantiene abierto mientras el proxy del servicio esté abierto y se cierre solo cuando se cierre el proxy del servicio.


Si el enlace de canal está basado en sesión y se produce un error en el canal subyacente, la máquina de Estados de proxy de servicio pasará al estado de [**error de estado de proxy de WS \_ Service \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) . En el caso de un enlace de canal no basado en sesión, un error en el canal subyacente no hace que el proxy pase al estado de **error de estado de proxy de servicio de WS \_ \_ \_ \_** .

Para obtener más información sobre el proxy del servicio y su relación con el estado, vea el tema [proxy del servicio](service-proxy.md) . Para obtener ejemplos de diferentes enlaces de canal, vea los ejemplos siguientes:

-   enlace de canal que no es de sesión, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   enlace de canal basado en sesión, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




