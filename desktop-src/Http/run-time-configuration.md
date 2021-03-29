---
title: Configuración de Run-Time
description: La API HTTP permite a las aplicaciones realizar la configuración dinámica en tiempo de ejecución.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b0a310f9fe86b2e6972aa2dff3d3b7fc05965
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665685"
---
# <a name="run-time-configuration"></a>Configuración de Run-Time

La API HTTP permite a las aplicaciones realizar la configuración dinámica en tiempo de ejecución. La configuración en tiempo de ejecución no es persistente, solo requiere privilegios de nivel bajo y solo afecta a la aplicación. La configuración de tiempo de ejecución puede incluir cualquiera de las siguientes actividades:

-   Inicializar el servicio HTTP y crear una sesión de servidor. Una aplicación inicializa el servicio HTTP mediante una llamada a la función [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) . El servidor debe inicializarse antes de que se pueda llamar a cualquier otra función de servidor. A continuación, la aplicación crea una sesión de servidor mediante una llamada a la función [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) . La sesión de servidor es un contenedor para las propiedades que se aplican a todos los grupos de direcciones URL que pertenecen a esa sesión de servidor. Normalmente cada allication tiene solo una sesión de servidor. Para obtener información sobre cómo establecer las propiedades de la sesión del servidor y en su ámbito, vea [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrando para las direcciones URL. Una vez creada la sesión del servidor, se puede registrar una aplicación para las direcciones URL mediante la creación de uno o varios grupos de direcciones URL. Un grupo de direcciones URL es un grupo de direcciones URL a las que se aplicarán las mismas propiedades. Una aplicación crea un grupo de direcciones URL mediante una llamada a la función [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) y, a continuación, agrega las direcciones URL deseadas llamando a la función [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) . Una vez que se ha registrado una aplicación para las direcciones URL mediante la creación de un grupo de direcciones URL y se ha asociado el grupo de direcciones URL con una cola de solicitudes (consulte [crear y enlazar a una cola de solicitudes](creating-and-binding-to-a-request-queue.md)), todas las solicitudes procedentes de estas direcciones URL se enrutan a la cola de solicitudes asociada a esa aplicación. Para obtener más información sobre las propiedades de grupo de URL de estableciendo, consulte [ **HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Habilitar características mediante la configuración de las propiedades del servidor HTTP, como la [autenticación](authentication-in-http-version-2-0.md), el [registro](server-side-logging-in-http-version-2-0.md), la configuración de QoS, los tiempos de espera, el estado habilitado y la información de enlace. Para obtener información sobre cómo establecer las propiedades, vea [**http \_ Server \_ Property**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




