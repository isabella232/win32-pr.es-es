---
title: Implementación de filtros de firewall para Teredo
description: Windows permite a las aplicaciones establecer una opción de socket que permite a las aplicaciones indicar una intención explícita de recibir tráfico de Teredo enviado al firewall de host a través de la plataforma de filtrado de Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001818"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Implementación de filtros de firewall para Teredo

Windows permite a las aplicaciones establecer una opción de socket que permite a las aplicaciones indicar una intención explícita de recibir tráfico de Teredo enviado al firewall de host a través de la plataforma de filtrado de Windows. En Windows, se usa una opción de socket para establecer un nivel de protección para permitir que una aplicación defina qué tipo de tráfico está dispuesto a recibir. Más concretamente, en escenarios que implican tráfico de Teredo, se especifica la opción de socket [ \_ IPV6 PROTECTION \_ LEVEL.](/windows/desktop/WinSock/ipv6-protection-level) Se recomienda que las implementaciones de firewall de host mantengan los siguientes filtros para permitir de forma selectiva el tráfico de Teredo para una aplicación, al tiempo que se bloquea el tráfico de forma predeterminada para cualquier aplicación sin una exención.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Filtro de bloque predeterminado para el tráfico perimetral recorrido

Un firewall de host siempre debe mantener un filtro de bloque predeterminado dentro de la capa de filtrado ALE AUTH RECV ACCEPT V6 para el tráfico que coincida con el tipo de interfaz Tunnel y Tunnel de \_ \_ \_ \_ **teredo** especificados.  Cuando se implementa, este filtro indica la presencia de un firewall de host que tenga en cuenta el recorrido perimetral en el sistema. Este filtro se ve como un contrato de API entre el firewall de host y Windows. De forma predeterminada, este filtro bloqueará el tráfico recorrido por el borde a cualquier aplicación.

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
> Las clases "Delivery", "Arrival" y "Next Hop" de condiciones de interfaz se usan para controlar un modelo de host débil y el reenvío de paquetes entre interfaces. En el ejemplo anterior se usa la clase "Delivery". Revise las [condiciones de filtrado disponibles en cada capa](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) de filtrado en la documentación del SDK de WFP, ya que el diseño de seguridad debe tener en cuenta cada caso.

 

## <a name="allow-filter-for-exempt-applications"></a>Permitir filtro para aplicaciones exentas

Si una aplicación está exenta de recibir tráfico de Teredo en un socket de escucha, se debe implementar un filtro de permiso dentro de la capa de filtrado \_ ALE AUTH RCV ACCEPT V6 en el \_ \_ firewall de \_ host. Es importante tener en cuenta que, en función de cómo configure la exención el usuario o la aplicación, el firewall de host puede incluir una opción de socket.

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

## <a name="dormancy-callout-filter"></a>Filtro de llamada de inactividad

El servicio Teredo de Windows implementa un modelo inactivo. En un momento dado, si ninguna aplicación escucha en un socket UDP o TCP con el recorrido perimetral habilitado, el servicio pasa a un estado inactivo. Para que el mecanismo inactivo funcione, el firewall de host debe mantener un filtro de llamada para cada aplicación exenta especificada dentro de la capa de filtrado ALE AUTH LISTEN V6 para TCP y la capa de filtrado \_ \_ \_ ALE \_ RESOURCE ASSIGNMENT \_ V6 para aplicaciones basadas en \_ UDP. En el ejemplo siguiente se muestra una llamada inactiva para una **aplicación TCP.**

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

 

 