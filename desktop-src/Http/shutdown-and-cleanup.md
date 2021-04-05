---
title: Apagado y limpieza
description: Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075827"
---
# <a name="shutdown-and-cleanup"></a>Apagado y limpieza

Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza:

-   Quite todas las direcciones URL registradas del grupo de direcciones URL mediante una llamada a la función [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para anular el registro de las direcciones URL registradas previamente en la llamada a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Cierre el grupo de direcciones URL mediante una llamada a la función [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Todos los grupos de direcciones URL creados en una sesión de servidor deben cerrarse antes de cerrar la sesión de servidor.
-   Cierre la sesión del servidor mediante una llamada a [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Cierre el identificador de la cola de solicitudes llamando a [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Finalice los recursos creados por la API del servidor HTTP mediante una llamada a la función [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con la configuración de marca coincidente para cada llamada que la aplicación realizó originalmente en [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Cada una de estas llamadas finaliza todos los recursos creados en la llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




