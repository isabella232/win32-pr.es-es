---
title: Referencia de api auxiliar de enrutamiento de conexiones a petición
description: En los temas siguientes se proporcionan detalles para el asistente de enrutamiento de conexiones a petición.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e046c1add8703e6603d925d2c80b03aab8d7eae3a352825e56ec907f3adb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685585"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Referencia de api auxiliar de enrutamiento de conexiones a petición

En los temas siguientes se proporcionan detalles para el asistente de enrutamiento de conexiones a petición.



| Referencia                                                                          | Descripción                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Busque un destino en la caché de solicitudes de ruta y, si se encuentra una coincidencia, devuelve el identificador de interfaz correspondiente.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Regístrese para recibir una notificación cuando se modifique la caché de solicitudes de ruta.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Anula el registro de las notificaciones y limpia los recursos.<br/>                                                                                                             |
| [**CONTEXTO DE \_ INTERFAZ \_ NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Contexto de interfaz que forma parte de la estructura [**NET \_ INTERFACE CONTEXT \_ \_ TABLE.**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)<br/>                                       |
| [**TABLA DE \_ CONTEXTO \_ DE INTERFAZ \_ NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Tabla de estructuras [**NET \_ INTERFACE \_ CONTEXT.**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Esta función recupera una tabla de contexto de interfaz para el nombre de host y el filtro de perfil de conexión especificados.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Esta función libera la tabla de contexto de interfaz recuperada mediante la [**función GetInterfaceContextTableForHostName.**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname)<br/> |



 

 

 





