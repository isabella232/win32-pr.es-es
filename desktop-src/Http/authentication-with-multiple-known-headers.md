---
title: Autenticación con varios encabezados conocidos
description: La estructura HTTP \_ MULTIPLE KNOWN HEADERS permite que las aplicaciones de servidor envíen varios \_ \_ desafíos de autenticación al cliente.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8fd2071626d8a12f046ac0c3b6c50fcffc794462d5109a89a974f441879bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950934"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticación con varios encabezados conocidos

La [**estructura HTTP MULTIPLE KNOWN HEADERS \_ \_ \_ permite**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) que las aplicaciones de servidor envíen varios desafíos de autenticación al cliente. Las aplicaciones pueden retar al cliente con un único esquema de autenticación si se proporciona el tipo de enumeración **HttpHeaderWwwAuthenticate** en el miembro **KnownHeaders** de la estructura [**HTTP RESPONSE \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_response_headers) contenida en [**HTTP \_ RESPONSE**](http-response.md). Sin embargo, cuando el servidor se enfrenta a varios esquemas de autenticación, la aplicación usa la estructura [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para proporcionar los tipos de autenticación.

Cuando la **marca HTTP RESPONSE INFO \_ \_ \_ FLAGS PRESERVE \_ \_ ORDER** está presente, HTTP envía los encabezados de autenticación en el orden especificado. Si la marca no está presente, HTTP ordena los esquemas de autenticación de más fuerte a más débil como se muestra a continuación:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Básico

Si el esquema de autenticación no es uno de estos esquemas, la aplicación debe especificar la marca **HTTP \_ RESPONSE INFO \_ \_ FLAGS PRESERVE \_ \_ ORDER.**

El **miembro KnownHeader** de [**HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) apunta a una matriz de [**estructuras HTTP KNOWN \_ \_ HEADER.**](/windows/desktop/api/Http/ns-http-http_known_header) El **miembro pRawValue** de la estructura **HTTP KNOWN \_ \_ HEADER** debe apuntar a una cadena que especifique el nombre del esquema. HTTP analiza la cadena para determinar el esquema y realiza una de las siguientes acciones:

-   Si la cadena contiene un tipo de autenticación desconocido, o si el tipo de autenticación no está habilitado en el grupo de configuración (el grupo de direcciones URL o la sesión de servidor) asociado a la solicitud, la API del servidor HTTP anexa la cadena de **pRawValue** al encabezado WWW-Authenticate. Por ejemplo, si la aplicación especifica un esquema de autenticación no admitido y **pRawValue** contiene la cadena "CustomAuthString", se anexa el texto siguiente al encabezado de autenticación:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Si la aplicación no tiene habilitada la autenticación básica y **pRawValue** contiene la cadena "Basic realm="BasicRealm"", el encabezado de autenticación contiene el texto siguiente:

    WWW-Authenticate: Basic realm="BasicRealm"

-   Si la cadena contiene un tipo de autenticación conocido y está presente en el grupo de configuración (el grupo de direcciones URL o la sesión de servidor) asociado a la solicitud, la API del servidor HTTP genera el encabezado WWW-Authenticate servidor. Por ejemplo, si la cadena especificada en **pRawValue** es "Digest" y Digest está habilitada en la sesión del servidor, la API del servidor HTTP anexa el texto siguiente al encabezado de autenticación:

    WWW-Authenticate: Digest realm=" testrealm@host.com "

Si el esquema del miembro **pRawValue** de [**HTTP KNOWN \_ \_ HEADER**](/windows/desktop/api/Http/ns-http-http_known_header) es Negotiate o NTLM, el nombre del esquema de autenticación es suficiente. Si el esquema especificado es Básico, el nombre de dominio se anexa al nombre de esquema; La aplicación no necesita proporcionar el nombre de dominio en **pRawValue**. Si el esquema especificado es Digest, HTTP llama a [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para generar el desafío que se anexa al nombre del esquema. Los parámetros del esquema Básico (dominio) y Resumen (dominio y nombre de dominio) se obtienen de la información de autenticación del grupo de configuración correspondiente.

Cuando la aplicación envía varios desafíos de autenticación al cliente en encabezados de solicitud desconocidos, la API del servidor HTTP los envía al cliente sin intervención. Sin embargo, no se recomienda este uso.

 

 




