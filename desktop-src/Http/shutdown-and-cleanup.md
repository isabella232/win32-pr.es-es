---
title: Apagado y limpieza
description: Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950695"
---
# <a name="shutdown-and-cleanup"></a>Apagado y limpieza

Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza:

-   Quite todas las direcciones URL registradas del grupo de direcciones URL llamando a la función [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para anular el registro de las direcciones URL registradas anteriormente en la llamada a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Cierre el grupo de direcciones URL mediante una llamada a [**la función HttpCloseUrlGroup.**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) Todos los grupos de direcciones URL creados en una sesión de servidor deben cerrarse antes de cerrar la sesión del servidor.
-   Cierre la sesión del servidor mediante una [**llamada a HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Cierre el identificador de la cola de solicitudes mediante [**una llamada a HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Finalice los recursos creados por la API del servidor HTTP llamando a la función [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con la configuración de marca correspondiente para cada llamada que la aplicación realizó originalmente a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Cada una de estas llamadas finaliza todos los recursos creados en la llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




