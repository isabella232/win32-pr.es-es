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
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="94feb-103">Referencia de API de la aplicación auxiliar de enrutamiento de conexión a petición</span><span class="sxs-lookup"><span data-stu-id="94feb-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="94feb-104">En los temas siguientes se proporcionan detalles de la aplicación auxiliar de enrutamiento de conexión a petición.</span><span class="sxs-lookup"><span data-stu-id="94feb-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="94feb-105">Referencia</span><span class="sxs-lookup"><span data-stu-id="94feb-105">Reference</span></span>                                                                          | <span data-ttu-id="94feb-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="94feb-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94feb-107">**OnDemandGetRoutingHint**</span><span class="sxs-lookup"><span data-stu-id="94feb-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="94feb-108">Busque un destino en la caché de solicitudes de ruta y, si se encuentra una coincidencia, devuelve el identificador de interfaz correspondiente.</span><span class="sxs-lookup"><span data-stu-id="94feb-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="94feb-109">**OnDemandRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="94feb-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="94feb-110">Regístrese para recibir una notificación cuando se modifique la memoria caché de solicitudes de ruta.</span><span class="sxs-lookup"><span data-stu-id="94feb-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="94feb-111">**OnDemandUnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="94feb-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="94feb-112">Anular el registro de las notificaciones y limpiar los recursos.</span><span class="sxs-lookup"><span data-stu-id="94feb-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="94feb-113">**contexto de la interfaz de red \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94feb-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="94feb-114">Contexto de interfaz que forma parte de la estructura de la [**\_ tabla de \_ contexto \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) de la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="94feb-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="94feb-115">**tabla de contexto de la interfaz de red \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94feb-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="94feb-116">Tabla de estructuras [**de \_ \_ contexto**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) de la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="94feb-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="94feb-117">**GetInterfaceContextTableForHostName**</span><span class="sxs-lookup"><span data-stu-id="94feb-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="94feb-118">Esta función recupera una tabla de contexto de interfaz para el nombre de host y el filtro de Perfil de conexión especificados.</span><span class="sxs-lookup"><span data-stu-id="94feb-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="94feb-119">**FreeInterfaceContextTable**</span><span class="sxs-lookup"><span data-stu-id="94feb-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="94feb-120">Esta función libera la tabla de contexto de la interfaz recuperada mediante la función [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .</span><span class="sxs-lookup"><span data-stu-id="94feb-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





