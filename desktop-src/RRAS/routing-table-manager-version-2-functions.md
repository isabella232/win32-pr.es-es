---
title: Funciones de Routing Table Manager versión 2
description: Las siguientes funciones se usan para interactuar con el administrador de tablas de enrutamiento.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- RRAS del servicio de enrutamiento y acceso remoto,Routing Table Manager versión 2, funciones
- RRAS RRAS, versión 2 de Routing Table Manager, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb7138b54ee0fa747c7d367c54d7a0fb893c3d2d451577932c669650a0fc76e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026925"
---
# <a name="routing-table-manager-version-2-functions"></a>Funciones de Routing Table Manager versión 2

Las siguientes funciones se usan para interactuar con el administrador de tablas de enrutamiento.

## <a name="registration-functions"></a>Funciones de registro

[**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a>Funciones de puntero opaco

[**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a>Funciones del método Export

[**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a>Controlar funciones de estructura de información

[**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a>Funciones de inserción y eliminación de tablas de enrutamiento

[**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[**RtmDeleteRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[**RtmGetRoutePointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a>Funciones de consulta de tabla de enrutamiento

[**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a>Funciones de inserción y eliminación de próximo salto

[**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[**RtmGetNextHopPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a>Funciones de enumeración de tablas de enrutamiento

[**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a>Funciones de notificación de cambios

[**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[**RtmIsMarkedForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a>Función Route List

[**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a>Control de funciones de administración

[**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




