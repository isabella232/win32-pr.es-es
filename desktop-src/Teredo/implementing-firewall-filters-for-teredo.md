---
title: Implementación de filtros de Firewall para Teredo
description: Windows permite a las aplicaciones establecer una opción de socket que permite a las aplicaciones indicar un intento explícito de recibir el tráfico Teredo que se envía al firewall del host a través de la plataforma de filtrado de Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792940"
---
# <a name="implementing-firewall-filters-for-teredo"></a><span data-ttu-id="63310-103">Implementación de filtros de Firewall para Teredo</span><span class="sxs-lookup"><span data-stu-id="63310-103">Implementing Firewall Filters for Teredo</span></span>

<span data-ttu-id="63310-104">Windows permite a las aplicaciones establecer una opción de socket que permite a las aplicaciones indicar un intento explícito de recibir el tráfico Teredo que se envía al firewall del host a través de la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="63310-104">Windows allows applications to set a socket option that allows applications to indicate an explicit intent to receive Teredo traffic sent to the host firewall via the Windows Filtering Platform.</span></span> <span data-ttu-id="63310-105">En Windows, se usa una opción de socket para establecer un nivel de protección para permitir que una aplicación defina qué tipo de tráfico está dispuesto a recibir.</span><span class="sxs-lookup"><span data-stu-id="63310-105">In Windows, a socket option for setting a protection level is used to allow an application to define what type of traffic it is willing to receive.</span></span> <span data-ttu-id="63310-106">Más concretamente, en escenarios que implican tráfico Teredo, se especifica la opción de socket de [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) .</span><span class="sxs-lookup"><span data-stu-id="63310-106">More specifically, in scenarios involving Teredo traffic, the [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option is specified.</span></span> <span data-ttu-id="63310-107">Se recomienda que las implementaciones de Firewall de host conserven los siguientes filtros para permitir de forma selectiva el tráfico Teredo para una aplicación, mientras se bloquea el tráfico de manera predeterminada para cualquier aplicación sin exención.</span><span class="sxs-lookup"><span data-stu-id="63310-107">It is recommended that host firewall implementations maintain the following filters to selectively allow Teredo traffic for an application, while blocking traffic by default for any application without an exemption.</span></span>

## <a name="default-block-filter-for-edge-traversed-traffic"></a><span data-ttu-id="63310-108">Filtro de bloque predeterminado para el tráfico atravesar perimetral</span><span class="sxs-lookup"><span data-stu-id="63310-108">Default Block Filter for Edge Traversed Traffic</span></span>

<span data-ttu-id="63310-109">Un firewall de host debe mantener siempre un filtro de bloque predeterminado dentro de la \_ \_ capa de filtrado de \_ aceptación V6 de autenticación Ale \_ para el tráfico que coincida con las condiciones de **Teredo** de tipo de **interfaz y túnel de tipo de interfaz** especificados.</span><span class="sxs-lookup"><span data-stu-id="63310-109">A host firewall must always maintain a default block filter within the ALE\_AUTH\_RECV\_ACCEPT\_V6 filtering layer for traffic matching the specified **Interface Type Tunnel** and **Tunnel Type Teredo** conditions.</span></span> <span data-ttu-id="63310-110">Cuando se implementa, este filtro indica la presencia de un firewall de host con reconocimiento de cruce perimetral en el sistema.</span><span class="sxs-lookup"><span data-stu-id="63310-110">When implemented, this filter indicates the presence of an edge traversal aware host firewall in the system.</span></span> <span data-ttu-id="63310-111">Este filtro se ve como un contrato de API entre el Firewall de host y Windows.</span><span class="sxs-lookup"><span data-stu-id="63310-111">This filter is viewed as an API contract between the host firewall and Windows.</span></span> <span data-ttu-id="63310-112">De forma predeterminada, este filtro bloqueará el tráfico que atraviesa el perímetro a cualquier aplicación.</span><span class="sxs-lookup"><span data-stu-id="63310-112">By default, this filter will block edge traversed traffic to any application.</span></span>

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> <span data-ttu-id="63310-113">Las clases "entrega", "llegada" y "próximo salto" de las condiciones de la interfaz se usan para controlar un modelo de host débil y el reenvío de paquetes a través de interfaces.</span><span class="sxs-lookup"><span data-stu-id="63310-113">The 'Delivery', 'Arrival', and 'Next Hop' classes of interface conditions are used to control a weak-host model and packet forwarding across interfaces.</span></span> <span data-ttu-id="63310-114">En el ejemplo anterior se emplea la clase ' Delivery '.</span><span class="sxs-lookup"><span data-stu-id="63310-114">The example above utilizes the 'Delivery' class.</span></span> <span data-ttu-id="63310-115">Revise las [condiciones de filtrado disponibles en cada nivel de filtrado](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) de la documentación del SDK de WFP, ya que el diseño de seguridad debe tener en cuenta cada caso.</span><span class="sxs-lookup"><span data-stu-id="63310-115">Please review [Filtering Conditions Available at Each Filtering Layer](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in the WFP SDK documentation, as your security design must take each case into consideration.</span></span>

 

## <a name="allow-filter-for-exempt-applications"></a><span data-ttu-id="63310-116">Permitir filtro para aplicaciones exentas</span><span class="sxs-lookup"><span data-stu-id="63310-116">Allow Filter for Exempt Applications</span></span>

<span data-ttu-id="63310-117">Si una aplicación está exenta de recibir tráfico Teredo en un socket de escucha, se debe implementar un filtro de permiso en la \_ capa de filtrado de aceptación V6 de la autenticación Ale \_ \_ \_ en el firewall del host.</span><span class="sxs-lookup"><span data-stu-id="63310-117">If an application is exempt from receiving Teredo traffic on a listening socket, a permit filter must be implemented within the ALE\_AUTH\_RCV\_ACCEPT\_V6 filtering layer on the host firewall.</span></span> <span data-ttu-id="63310-118">Es importante tener en cuenta que, en función de cómo esté configurada la exención por parte del usuario o la aplicación, el firewall del host puede incluir una opción de socket.</span><span class="sxs-lookup"><span data-stu-id="63310-118">It is important to note that depending on how the exemption is configured by the user or application, the host firewall can include a socket option.</span></span>

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a><span data-ttu-id="63310-119">Filtro de llamada de inactividad</span><span class="sxs-lookup"><span data-stu-id="63310-119">Dormancy Callout Filter</span></span>

<span data-ttu-id="63310-120">El servicio Teredo en Windows implementa un modelo inactividad.</span><span class="sxs-lookup"><span data-stu-id="63310-120">The Teredo service in Windows implements a dormancy model.</span></span> <span data-ttu-id="63310-121">En un momento dado, si no hay ninguna aplicación escuchando en un socket UDP o TCP con el cruce seguro del perímetro habilitado, el servicio pasa a un estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="63310-121">At any given time, if no applications are listening on a UDP or TCP socket with edge traversal enabled, the service moves to a dormant state.</span></span> <span data-ttu-id="63310-122">Para que el mecanismo inactividad funcione, el firewall del host debe mantener un filtro de llamada para cada aplicación exenta especificada dentro \_ del \_ \_ nivel de filtrado de escucha de autenticación Ale V6 para TCP, y el \_ nivel de filtrado de asignación de recursos Ale \_ \_ V6 para aplicaciones basadas en UDP.</span><span class="sxs-lookup"><span data-stu-id="63310-122">For the dormancy mechanism to work, the host firewall must maintain a callout filter for each exempt application specified within the ALE\_AUTH\_LISTEN\_V6 filtering layer for TCP, and ALE\_RESOURCE\_ASSIGNMENT\_V6 filtering layer for UDP based applications.</span></span> <span data-ttu-id="63310-123">En el siguiente ejemplo se muestra una llamada a inactividad para una aplicación **TCP** .</span><span class="sxs-lookup"><span data-stu-id="63310-123">The following sample below demonstrates a dormancy callout for a **TCP** application.</span></span>

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 