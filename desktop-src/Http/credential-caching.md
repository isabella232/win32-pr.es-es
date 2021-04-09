---
title: Caché de credenciales
description: Caché de credenciales
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994417"
---
# <a name="credential-caching"></a>Caché de credenciales

## <a name="credential-caching-on-ntlm-ka-connections"></a>Almacenamiento en caché de credenciales en conexiones de NTLM KA

La API del servidor HTTP almacena en caché las credenciales solo en conexiones Keep-Alive (KA) para la autenticación NTLM. De forma predeterminada, la API del servidor HTTP almacena en caché las credenciales obtenidas en la primera solicitud enviada en una conexión KA. El cliente puede enviar solicitudes posteriores en conexiones KA sin un encabezado de autorización y obtener autenticación basada en el contexto establecido previamente. En este caso, la API del servidor HTTP envía el token basado en la credencial almacenada en caché a la aplicación. Las credenciales de una solicitud enviada por un proxy no se almacenan en caché. La aplicación deshabilita el almacenamiento en caché de credenciales NTLM al establecer la marca **DisableNTLMCredentialCaching** en la estructura de [**\_ información de \_ autenticación \_ del servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) que se proporciona en las llamadas a HttpSetServerSessionProperty o HttpSetUrlGroupProperty. Cuando se deshabilita el almacenamiento en caché de credenciales, la API del servidor HTTP descarta las credenciales almacenadas en caché y realiza la autenticación para cada solicitud.

## <a name="ntlm-credential-caching-for-specific-urls"></a>Almacenamiento en caché de credenciales NTLM para direcciones URL específicas

La aplicación determina si las credenciales de solicitud devueltas por la API del servidor HTTP se almacenan en caché mediante la inspección del parámetro flags de la estructura de información de autenticación de la \_ solicitud HTTP \_ \_ . Este parámetro indica \_ \_ \_ el token de la marca de autenticación de la solicitud HTTP \_ \_ para \_ CRED almacenada \_ cuando el token NTLM devuelto se recuperó de la memoria caché. El almacenamiento en caché de credenciales se especifica en un grupo de direcciones URL para todas las direcciones URL del grupo. No se admite el almacenamiento en caché de credenciales por dirección URL; sin embargo, las aplicaciones pueden determinar si se aceptan o rechazan las credenciales almacenadas en caché por dirección URL comprobando el \_ \_ \_ token de marca de autenticación de la solicitud HTTP \_ \_ para \_ \_ la marca CRED almacenada en caché en la estructura de información de autenticación de la \_ solicitud HTTP \_ \_ . La aplicación rechaza las credenciales almacenadas en caché enviando un desafío de autenticación 401 al cliente. Después, el cliente vuelve a enviar la solicitud con los encabezados de autorización, lo que desencadena un nuevo protocolo de enlace de autenticación con la API del servidor HTTP.

## <a name="basic-authentication"></a>Autenticación básica

Cuando se incluye un encabezado de autenticación básica en la solicitud, la API del servidor HTTP analiza el encabezado para obtener el nombre de usuario y la contraseña. A continuación, el nombre de usuario se analiza en las partes de usuario y dominio. La API del servidor HTTP almacena en caché el token de acceso, obtenido para la autenticación básica, según el nombre de usuario y la clave de dominio. Cuando se recibe una nueva solicitud, la API del servidor HTTP recupera el token de acceso en función del nombre de usuario y el dominio. A continuación, la contraseña de la solicitud se comprueba con la contraseña almacenada en caché. El token de acceso almacenado en caché se elimina cuando se alcanza el límite de tiempo de vida (TTL).

 

 




