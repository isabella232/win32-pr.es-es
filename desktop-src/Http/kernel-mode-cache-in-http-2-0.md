---
title: Caché de modo kernel
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076262"
---
# <a name="kernel-mode-cache"></a>Caché de modo kernel

La API del servidor HTTP versión 2,0 permite a las aplicaciones almacenar en caché las respuestas con contenido estático en modo kernel. Se consigue un mayor rendimiento cuando las solicitudes se atienden desde la memoria caché del kernel sin pasar al modo de usuario.

La API del servidor HTTP aplica las configuraciones de propiedades adecuadas a todas las solicitudes atendidas desde la caché del kernel, incluidas las respuestas de registro. Sin embargo, las solicitudes que requieren autenticación no se servirán desde la memoria caché.

La API del servidor HTTP limita la memoria caché del modo kernel a las solicitudes que cumplen las condiciones siguientes:

-   El verbo de solicitud es GET y se ha recibido toda la solicitud.
-   La solicitud no debe tener un cuerpo de entidad.
-   El protocolo HTTP es la versión 1,0 o posterior.
-   El encabezado "translate: f" no está presente.
-   No hay encabezados que no sean "expect: 100-Continue".
-   El encabezado Authorization no está presente.
-   Los encabezados Range y If-Range no están presentes.

Además de las restricciones de la solicitud, la respuesta también debe cumplir las siguientes condiciones:

-   De forma predeterminada, el tamaño de la respuesta está limitado a 256 KB. Para cambiar el tamaño de la respuesta almacenada en caché, establezca el valor del registro **UriMaxUriBytes** en el número de bytes necesario.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   La respuesta completa debe proporcionarse en una única llamada a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).
-   No se debe suprimir el encabezado de fecha de la respuesta.
-   Si el encabezado last-modified está presente, el valor del encabezado debe tener la sintaxis correcta. El valor de hora de este encabezado se usa para la comprobación del control de caché.
-   La memoria caché del modo kernel tiene espacio suficiente para almacenar la respuesta.

De forma predeterminada, está habilitada la caché de respuesta de modo kernel. Si no se cumple alguna de las condiciones para la solicitud o respuesta mencionada anteriormente, se enviará la respuesta, pero no se almacenará en caché. En la API del servidor HTTP versión 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) incluye un parámetro *pCachePolicy* opcional para pasar la estructura de la [**\_ \_ Directiva de caché http**](/windows/desktop/api/Http/ns-http-http_cache_policy) . Las aplicaciones usan la estructura de la Directiva de caché para configurar la memoria caché.

 

 




