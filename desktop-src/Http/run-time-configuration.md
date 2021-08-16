---
title: Run-Time configuración
description: La API HTTP permite a las aplicaciones realizar la configuración dinámica en tiempo de ejecución.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b240438ada7fce186f334df3175b8ecc5b557626c5f1f085cdf82965fb32365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393757"
---
# <a name="run-time-configuration"></a>Run-Time configuración

La API HTTP permite a las aplicaciones realizar la configuración dinámica en tiempo de ejecución. La configuración en tiempo de ejecución no es persistente, solo requiere privilegios de bajo nivel y solo afecta a la aplicación. La configuración en tiempo de ejecución puede incluir cualquiera de las actividades siguientes:

-   Inicializar el servicio HTTP y crear una sesión de servidor. Una aplicación inicializa el servicio HTTP llamando a la [**función HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize) El servidor debe inicializarse antes de que se pueda llamar a cualquier otra función del servidor. A continuación, la aplicación crea una sesión de servidor mediante una llamada a [**la función HttpCreateServerSession.**](/windows/desktop/api/Http/nf-http-httpcreateserversession) La sesión del servidor es un contenedor de propiedades que se aplican a todos los grupos de direcciones URL que pertenecen a esa sesión de servidor. Normalmente, cada alication solo tiene una sesión de servidor. Para obtener información sobre cómo establecer las propiedades de sesión del servidor y sobre su ámbito, [**vea HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registro de direcciones URL. Una vez creada la sesión del servidor, una aplicación puede registrarse para obtener direcciones URL mediante la creación de uno o varios grupos de direcciones URL. Un grupo de direcciones URL es un grupo de direcciones URL a los que se aplicarán las mismas propiedades. Una aplicación crea un grupo de direcciones URL llamando a la función [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) y, a continuación, agrega las direcciones URL deseadas llamando a la [**función HttpAddUrlToUrlGroup.**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) Una vez que una aplicación se ha registrado para las direcciones URL mediante la creación de un grupo de direcciones URL y ha asociado el grupo de direcciones URL a una cola de solicitudes (consulte Creación y enlace a una cola de solicitudes), todas las solicitudes procedentes de estas direcciones URL se enruta a la cola de solicitudes asociada [a](creating-and-binding-to-a-request-queue.md)esa aplicación. Para obtener más información sobre cómo establecer las propiedades del grupo de direcciones URL, [ **vea HttpSetUrlGroupProperty.**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Habilitar características estableciendo las propiedades [](authentication-in-http-version-2-0.md)del servidor HTTP, como la autenticación, el [registro,](server-side-logging-in-http-version-2-0.md)la configuración de QOS, los tiempos de espera, el estado habilitado y la información de enlace. Para obtener información sobre cómo establecer propiedades, [**vea HTTP \_ SERVER \_ PROPERTY**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




