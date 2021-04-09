---
title: Referencia de API de la aplicación auxiliar de enrutamiento de conexión a petición
description: En los temas siguientes se proporcionan detalles de la aplicación auxiliar de enrutamiento de conexión a petición.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148855"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Referencia de API de la aplicación auxiliar de enrutamiento de conexión a petición

En los temas siguientes se proporcionan detalles de la aplicación auxiliar de enrutamiento de conexión a petición.



| Referencia                                                                          | Descripción                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Busque un destino en la caché de solicitudes de ruta y, si se encuentra una coincidencia, devuelve el identificador de interfaz correspondiente.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Regístrese para recibir una notificación cuando se modifique la memoria caché de solicitudes de ruta.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Anular el registro de las notificaciones y limpiar los recursos.<br/>                                                                                                             |
| [**contexto de la interfaz de red \_ \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Contexto de interfaz que forma parte de la estructura de la [**\_ tabla de \_ contexto \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) de la interfaz de red.<br/>                                       |
| [**tabla de contexto de la interfaz de red \_ \_ \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Tabla de estructuras [**de \_ \_ contexto**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) de la interfaz de red.<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Esta función recupera una tabla de contexto de interfaz para el nombre de host y el filtro de Perfil de conexión especificados.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Esta función libera la tabla de contexto de la interfaz recuperada mediante la función [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .<br/> |



 

 

 





