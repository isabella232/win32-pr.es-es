---
title: Autenticación con varios encabezados conocidos
description: La \_ estructura http Multiple \_ knowd \_ headers permite que las aplicaciones de servidor envíen varios desafíos de autenticación al cliente.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685540"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticación con varios encabezados conocidos

La estructura [**http \_ Multiple \_ knowd \_ headers**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) permite que las aplicaciones de servidor envíen varios desafíos de autenticación al cliente. Las aplicaciones pueden desafiar al cliente con un esquema de autenticación único proporcionando el tipo de enumeración **HttpHeaderWwwAuthenticate** en el miembro **KnownHeaders** de la estructura de [**\_ \_ encabezados de respuesta http**](/windows/desktop/api/Http/ns-http-http_response_headers) que se incluye en la [**\_ respuesta http**](http-response.md). Sin embargo, cuando el servidor desafía con varios esquemas de autenticación, la aplicación utiliza la estructura de [**\_ varios \_ \_ encabezados conocidos de http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para proporcionar los tipos de autenticación.

Cuando la marca de **información de respuesta http conserva la marca de \_ \_ \_ \_ \_ orden** , http envía los encabezados de autenticación en el orden especificado. Si el marcador no está presente, HTTP ordena los esquemas de autenticación del más fuerte al más débil como se indica a continuación:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Básico

Si el esquema de autenticación no es uno de estos esquemas, la aplicación debe especificar las **\_ marcas de información de respuesta HTTP \_ \_ \_ para conservar \_** el indicador de orden.

El miembro **KnownHeader** de [**http \_ Multiple \_ knowers \_**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) apunta a una matriz de estructuras [**de \_ \_ encabezado conocidas de http**](/windows/desktop/api/Http/ns-http-http_known_header) . El miembro **pRawValue** de la estructura de **\_ \_ encabezado conocida http** debe apuntar a una cadena que especifique el nombre del esquema. HTTP analiza la cadena para determinar el esquema y realiza una de las acciones siguientes:

-   Si la cadena contiene un tipo de autenticación desconocido, o si el tipo de autenticación no está habilitado en el grupo de configuración (ya sea el grupo de direcciones URL o la sesión del servidor) asociado a la solicitud, la API del servidor HTTP anexa la cadena de **pRawValue** al encabezado WWW-Authenticate. Por ejemplo, si la aplicación especifica un esquema de autenticación no admitido y **pRawValue** contiene la cadena "CustomAuthString", el texto siguiente se anexa al encabezado de autenticación:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Si la aplicación no tiene habilitada la autenticación básica y **pRawValue** contiene la cadena "Basic realm =" BasicRealm "", el encabezado de autenticación contiene el siguiente texto:

    WWW-Authenticate: dominio básico = "BasicRealm"

-   Si la cadena contiene un tipo de autenticación conocido y está presente en el grupo de configuración (ya sea el grupo de direcciones URL o la sesión del servidor) asociado a la solicitud, la API del servidor HTTP genera el encabezado WWW-Authenticate. Por ejemplo, si la cadena especificada en **pRawValue** es "Digest" y la síntesis está habilitada en la sesión del servidor, la API del servidor http anexa el siguiente texto al encabezado de autenticación:

    WWW-Authenticate: Digest realm = " testrealm@host.com "

Si el esquema del miembro **pRawValue** del [**\_ \_ encabezado conocido de http**](/windows/desktop/api/Http/ns-http-http_known_header) es Negotiate o NTLM, el nombre del esquema de autenticación es suficiente. Si el esquema especificado es básico, el nombre de dominio Kerberos se anexa al nombre de esquema; no es necesario que la aplicación proporcione el nombre de dominio Kerberos en **pRawValue**. Si el esquema especificado es Digest, HTTP llama a [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para generar el desafío que se anexa al nombre de esquema. Los parámetros para el esquema básico (dominio Kerberos) y el esquema de resumen (dominio y dominio) se obtienen de la información de autenticación del grupo de configuración correspondiente.

Cuando la aplicación envía varios desafíos de autenticación al cliente en encabezados de solicitud desconocidos, la API del servidor HTTP los envía al cliente sin intervención. Sin embargo, no se recomienda este uso.

 

 




