---
title: Funciones de administración de RAS
description: En esta documentación se describen las funciones RRAS que se usan para desarrollar software para administrar conexiones de acceso telefónico RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357614"
---
# <a name="ras-administration-functions"></a>Funciones de administración de RAS

En esta documentación se describen las funciones RRAS que se usan para desarrollar software para administrar conexiones de acceso telefónico RAS. Estas funciones incluyen:

-   [**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [**MprAdminConnectionEnumEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [**MprAdminConnectionGetInfoEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [**MprAdminConnectionRemoveQuarantine**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

Se usan funciones adicionales para la administración de RAS y la administración de enrutadores. Las siguientes funciones documentadas en la referencia de las [funciones de administración del enrutador](router-administration-functions.md) :

-   [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Para implementar un archivo DLL de administración de RAS, utilice las funciones descritas en el tema siguiente:

-   [Funciones de DLL de administración de RAS](ras-admin-dll-functions.md)

Para administrar usuarios de un servidor RAS, use las funciones descritas en el tema siguiente:

-   [Funciones de administración de usuarios de RAS](ras-user-administration-functions.md)

 

 




