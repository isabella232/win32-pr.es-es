---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glosario (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910846"
---
# <a name="glossary-winhttp"></a>Glosario (WinHTTP)

<dl> <dt>

<span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**datos de autenticación**
</dt> <dd>

Bloque de datos específico del esquema que se intercambia entre el servidor y el cliente durante la autenticación. Para demostrar su identidad, el cliente cifra algunos o todos los datos con un nombre de usuario y una contraseña. El cliente envía los datos cifrados al servidor, que descifra los datos y los compara con el original. Si los datos descifrados coinciden con los datos originales, el cliente se autentica.

</dd> <dt>

<span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**codificación Base64**
</dt> <dd>

Esquema usado para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados. A veces se conoce como codificación de 3 a 4. Cada 6 bits del grupo de 24 bits se utiliza como índice en una tabla de asignación (el alfabeto Base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea limitadas a 76 caracteres.

</dd> <dt>

<span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**almacén de certificados**
</dt> <dd>

Normalmente, almacenamiento permanente en el que se almacenan los certificados, las listas de revocación de certificados (CRL) y las listas de certificados de confianza (CTL). Un almacén de certificados también puede ser temporal cuando se trabaja con certificados basados en sesión.

</dd> <dt>

<span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**
</dt> <dd>

Capacidad para que un sitio de Microsoft Passport participante proporcione sus propios elementos de personalización de marca y explicaciones en las páginas de servicio de red de Passport. La personalización de marca incluye la personalización de la apariencia, el texto específico y el comportamiento específico en las páginas de red de Passport.

</dd> <dt>

<span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**Página de códigos**
</dt> <dd>

Tabla que relaciona los códigos de caracteres binarios usados por un programa con las teclas del teclado o con la apariencia de los caracteres en el monitor. El uso de páginas de códigos es una manera de proporcionar compatibilidad con los juegos de caracteres y las distribuciones de teclado que se usan en diferentes países y regiones. Puede configurar dispositivos como el monitor y el teclado para usar una página de códigos específica y cambiar de una página de códigos (como Estados Unidos) a otra (como Portugal) en la solicitud del usuario.

</dd> <dt>

<span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**
</dt> <dd>

El verbo HTTP (o el método HTTP) es una instrucción enviada en un mensaje de solicitud que notifica a un servidor HTTP de la acción que debe realizar en el recurso especificado. Por ejemplo, "GET" especifica que un recurso se recupera del servidor. Los verbos comunes incluyen "GET", "POST" y "HEAD". Para obtener más información y una lista completa de los verbos HTTP estándar, vea la especificación HTTP/1.1.

</dd> <dt>

<span id="term_ticket"></span><span id="TERM_TICKET"></span>**vale**
</dt> <dd>

Cookie que contiene un perfil de usuario para la autenticación de Passport. Cada vale corresponde a una dirección URL. El servidor de inicio de sesión de una entidad de dominio de Passport proporciona vales que el cliente envía a un miembro de Passport para la autenticación.

</dd> <dt>

<span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente de usuario**
</dt> <dd>

El agente de usuario es la aplicación cliente que solicita un documento desde un servidor HTTP. Cuando el cliente envía una solicitud a un servidor HTTP, normalmente envía el nombre del agente de usuario con el encabezado de solicitud para que el servidor pueda determinar las capacidades del software cliente.

</dd> </dl>

 

 



