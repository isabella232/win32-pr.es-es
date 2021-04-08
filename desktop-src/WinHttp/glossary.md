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
# <a name="glossary-winhttp"></a><span data-ttu-id="cae3b-103">Glosario (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="cae3b-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="cae3b-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**datos de autenticación**</span><span class="sxs-lookup"><span data-stu-id="cae3b-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-105">Bloque de datos específico del esquema que se intercambia entre el servidor y el cliente durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="cae3b-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="cae3b-106">Para demostrar su identidad, el cliente cifra algunos o todos los datos con un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="cae3b-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="cae3b-107">El cliente envía los datos cifrados al servidor, que descifra los datos y los compara con el original.</span><span class="sxs-lookup"><span data-stu-id="cae3b-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="cae3b-108">Si los datos descifrados coinciden con los datos originales, el cliente se autentica.</span><span class="sxs-lookup"><span data-stu-id="cae3b-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**codificación Base64**</span><span class="sxs-lookup"><span data-stu-id="cae3b-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-110">Esquema usado para transmitir datos binarios.</span><span class="sxs-lookup"><span data-stu-id="cae3b-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="cae3b-111">Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados.</span><span class="sxs-lookup"><span data-stu-id="cae3b-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="cae3b-112">A veces se conoce como codificación de 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="cae3b-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="cae3b-113">Cada 6 bits del grupo de 24 bits se utiliza como índice en una tabla de asignación (el alfabeto Base64) para obtener un carácter para los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="cae3b-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="cae3b-114">Los datos codificados tienen longitudes de línea limitadas a 76 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cae3b-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**almacén de certificados**</span><span class="sxs-lookup"><span data-stu-id="cae3b-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-116">Normalmente, almacenamiento permanente en el que se almacenan los certificados, las listas de revocación de certificados (CRL) y las listas de certificados de confianza (CTL).</span><span class="sxs-lookup"><span data-stu-id="cae3b-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="cae3b-117">Un almacén de certificados también puede ser temporal cuando se trabaja con certificados basados en sesión.</span><span class="sxs-lookup"><span data-stu-id="cae3b-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span><span class="sxs-lookup"><span data-stu-id="cae3b-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-119">Capacidad para que un sitio de Microsoft Passport participante proporcione sus propios elementos de personalización de marca y explicaciones en las páginas de servicio de red de Passport.</span><span class="sxs-lookup"><span data-stu-id="cae3b-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="cae3b-120">La personalización de marca incluye la personalización de la apariencia, el texto específico y el comportamiento específico en las páginas de red de Passport.</span><span class="sxs-lookup"><span data-stu-id="cae3b-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**Página de códigos**</span><span class="sxs-lookup"><span data-stu-id="cae3b-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-122">Tabla que relaciona los códigos de caracteres binarios usados por un programa con las teclas del teclado o con la apariencia de los caracteres en el monitor.</span><span class="sxs-lookup"><span data-stu-id="cae3b-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="cae3b-123">El uso de páginas de códigos es una manera de proporcionar compatibilidad con los juegos de caracteres y las distribuciones de teclado que se usan en diferentes países y regiones.</span><span class="sxs-lookup"><span data-stu-id="cae3b-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="cae3b-124">Puede configurar dispositivos como el monitor y el teclado para usar una página de códigos específica y cambiar de una página de códigos (como Estados Unidos) a otra (como Portugal) en la solicitud del usuario.</span><span class="sxs-lookup"><span data-stu-id="cae3b-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**</span><span class="sxs-lookup"><span data-stu-id="cae3b-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-126">El verbo HTTP (o el método HTTP) es una instrucción enviada en un mensaje de solicitud que notifica a un servidor HTTP de la acción que debe realizar en el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="cae3b-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="cae3b-127">Por ejemplo, "GET" especifica que un recurso se recupera del servidor.</span><span class="sxs-lookup"><span data-stu-id="cae3b-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="cae3b-128">Los verbos comunes incluyen "GET", "POST" y "HEAD".</span><span class="sxs-lookup"><span data-stu-id="cae3b-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="cae3b-129">Para obtener más información y una lista completa de los verbos HTTP estándar, vea la especificación HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="cae3b-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**vale**</span><span class="sxs-lookup"><span data-stu-id="cae3b-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-131">Cookie que contiene un perfil de usuario para la autenticación de Passport.</span><span class="sxs-lookup"><span data-stu-id="cae3b-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="cae3b-132">Cada vale corresponde a una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="cae3b-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="cae3b-133">El servidor de inicio de sesión de una entidad de dominio de Passport proporciona vales que el cliente envía a un miembro de Passport para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="cae3b-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="cae3b-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente de usuario**</span><span class="sxs-lookup"><span data-stu-id="cae3b-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="cae3b-135">El agente de usuario es la aplicación cliente que solicita un documento desde un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="cae3b-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="cae3b-136">Cuando el cliente envía una solicitud a un servidor HTTP, normalmente envía el nombre del agente de usuario con el encabezado de solicitud para que el servidor pueda determinar las capacidades del software cliente.</span><span class="sxs-lookup"><span data-stu-id="cae3b-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



