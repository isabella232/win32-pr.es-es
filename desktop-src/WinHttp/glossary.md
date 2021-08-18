---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glosario (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2064d9b7424971e2be286b18129fa3b4109fb64a03fa26ababc152a5cf0b64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133208"
---
# <a name="glossary-winhttp"></a>Glosario (WinHTTP)

<dl> <dt>

<span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**datos de autenticación**
</dt> <dd>

Bloque de datos específico del esquema que se intercambia entre el servidor y el cliente durante la autenticación. Para demostrar su identidad, el cliente cifra algunos o todos estos datos con un nombre de usuario y una contraseña. El cliente envía los datos cifrados al servidor, que descifra los datos y los compara con el original. Si los datos descifrados coinciden con los datos originales, el cliente se autentica.

</dd> <dt>

<span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**Codificación base64**
</dt> <dd>

Esquema utilizado para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits y asigna estos datos a cuatro caracteres codificados. A veces se conoce como codificación 3 a 4. Cada 6 bits del grupo de 24 bits se usa como índice en una tabla de asignación (el alfabeto base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea limitadas a 76 caracteres.

</dd> <dt>

<span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**almacén de certificados**
</dt> <dd>

Normalmente, el almacenamiento permanente donde se almacenan los certificados, las listas de revocación de certificados (CRL) y las listas de confianza de certificados (CTL). Un almacén de certificados también puede ser temporal cuando se trabaja con certificados basados en sesión.

</dd> <dt>

<span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**
</dt> <dd>

Capacidad de un sitio Microsoft Passport participante para proporcionar sus propios elementos de personal de marca y explicaciones en las páginas del servicio de red de Passport. La marca de marca incluye la personalización de la apariencia, el texto específico y el comportamiento específico en las páginas de red de Passport.

</dd> <dt>

<span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**página de códigos**
</dt> <dd>

Tabla que relaciona los códigos de caracteres binarios usados por un programa con las teclas del teclado o con la apariencia de caracteres en el monitor. El uso de páginas de códigos es una manera de proporcionar compatibilidad con juegos de caracteres y diseños de teclado usados en diferentes países y regiones. Puede configurar dispositivos como el monitor y el teclado para usar una página de códigos específica y cambiar de una página de códigos (como Estados Unidos) a otra (como Portugal) a petición del usuario.

</dd> <dt>

<span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**
</dt> <dd>

El verbo HTTP (o método HTTP) es una instrucción enviada en un mensaje de solicitud que notifica a un servidor HTTP la acción que se debe realizar en el recurso especificado. Por ejemplo, "GET" especifica que se está recuperando un recurso del servidor. Los verbos comunes incluyen "GET", "POST" y "HEAD". Para obtener más información y una lista completa de verbos HTTP estándar, consulte la especificación HTTP/1.1.

</dd> <dt>

<span id="term_ticket"></span><span id="TERM_TICKET"></span>**Boleto**
</dt> <dd>

Cookie que contiene un perfil de usuario para la autenticación de Passport. Cada vale corresponde a una dirección URL. El servidor de inicio de sesión de una autoridad de dominio de Passport proporciona vales que el cliente envía a un miembro de Passport para la autenticación.

</dd> <dt>

<span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente de usuario**
</dt> <dd>

El agente de usuario es la aplicación cliente que solicita un documento desde un servidor HTTP. Cuando el cliente envía una solicitud a un servidor HTTP, normalmente envía el nombre del agente de usuario con el encabezado de solicitud para que el servidor pueda determinar las funcionalidades del software cliente.

</dd> </dl>

 

 



