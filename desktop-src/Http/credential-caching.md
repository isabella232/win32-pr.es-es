---
title: Caché de credenciales
description: Caché de credenciales
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9354a1637e44ccb63c7f40db1cb7e8bc91aa6f42baf79712370531f627236cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047345"
---
# <a name="credential-caching"></a>Caché de credenciales

## <a name="credential-caching-on-ntlm-ka-connections"></a>Almacenamiento en caché de credenciales en conexiones NTLM KA

La API del servidor HTTP almacena en caché las credenciales solo en Keep-Alive (KA) para la autenticación NTLM. De forma predeterminada, la API del servidor HTTP almacena en caché las credenciales obtenidas en la primera solicitud enviada en una conexión KA. El cliente puede enviar solicitudes posteriores en conexiones KA sin un encabezado de autorización y obtener la autenticación en función del contexto establecido anteriormente. En este caso, la API del servidor HTTP envía el token en función de la credencial almacenada en caché a la aplicación. Las credenciales de una solicitud enviada por un proxy no se almacenan en caché. La aplicación deshabilita el almacenamiento en caché de credenciales NTLM estableciendo la marca **DisableNTLMCredentialCaching** en la estructura [**HTTP SERVER AUTHENTICATION \_ \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) que se proporciona en las llamadas a HttpSetServerSessionProperty o HttpSetUrlGroupProperty. Cuando el almacenamiento en caché de credenciales está deshabilitado, la API del servidor HTTP descarta las credenciales almacenadas en caché y realiza la autenticación para cada solicitud.

## <a name="ntlm-credential-caching-for-specific-urls"></a>Almacenamiento en caché de credenciales NTLM para direcciones URL específicas

La aplicación determina si las credenciales de solicitud devueltas por la API del servidor HTTP se almacenan en caché inspeccionando el parámetro Flags de la estructura HTTP \_ REQUEST \_ AUTH \_ INFO. Este parámetro indica HTTP \_ REQUEST AUTH FLAG TOKEN FOR CACHED CRED cuando se recuperó el token NTLM devuelto \_ de la memoria \_ \_ \_ \_ \_ caché. El almacenamiento en caché de credenciales se especifica en un grupo de direcciones URL para todas las direcciones URL del grupo. No se admite el almacenamiento en caché de credenciales por dirección URL; sin embargo, las aplicaciones pueden determinar si se aceptan o rechazan las credenciales almacenadas en caché por dirección URL mediante la comprobación de la marca HTTP REQUEST AUTH FLAG TOKEN FOR CACHED CRED en la estructura \_ \_ HTTP REQUEST \_ \_ \_ \_ \_ \_ \_ AUTH \_ INFO. La aplicación rechaza las credenciales almacenadas en caché mediante el envío de un desafío de autenticación 401 al cliente. A continuación, el cliente vuelve a enviar la solicitud con los encabezados de autorización, desencadenando un nuevo protocolo de enlace de autenticación con la API del servidor HTTP.

## <a name="basic-authentication"></a>Autenticación básica

Cuando se incluye un encabezado de autenticación básico en la solicitud, la API del servidor HTTP analiza el encabezado para obtener el nombre de usuario y la contraseña. A continuación, el nombre de usuario se analiza en las partes de usuario y dominio. La API del servidor HTTP almacena en caché el token de acceso, obtenido para la autenticación básica, en función del nombre de usuario y la clave de dominio. Cuando se recibe una nueva solicitud, la API del servidor HTTP recupera el token de acceso en función del nombre de usuario y el dominio. La contraseña de la solicitud se comprueba con la contraseña almacenada en caché. El token de acceso almacenado en caché se elimina cuando se alcanza el límite de período de vida (TTL).

 

 




