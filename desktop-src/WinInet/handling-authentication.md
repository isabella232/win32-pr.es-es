---
title: Control de la autenticación
description: Algunos servidores proxy y requieren autenticación antes de conceder acceso a los recursos de Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380859"
---
# <a name="handling-authentication"></a><span data-ttu-id="79756-103">Control de la autenticación</span><span class="sxs-lookup"><span data-stu-id="79756-103">Handling Authentication</span></span>

<span data-ttu-id="79756-104">Algunos servidores proxy y requieren autenticación antes de conceder acceso a los recursos de Internet.</span><span class="sxs-lookup"><span data-stu-id="79756-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="79756-105">Las funciones de WinINet admiten la autenticación de servidor y proxy para sesiones HTTP.</span><span class="sxs-lookup"><span data-stu-id="79756-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="79756-106">La autenticación de servidores ftp debe controlarse mediante la [**función InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)</span><span class="sxs-lookup"><span data-stu-id="79756-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="79756-107">Actualmente, no se admite la autenticación de puerta de enlace FTP.</span><span class="sxs-lookup"><span data-stu-id="79756-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="79756-108">Acerca de la autenticación HTTP</span><span class="sxs-lookup"><span data-stu-id="79756-108">About HTTP Authentication</span></span>

<span data-ttu-id="79756-109">Si se requiere autenticación, la aplicación cliente recibe un código de estado 401, si el servidor requiere autenticación, o 407, si el proxy requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="79756-110">Con el código de estado, el proxy o servidor envía uno o varios encabezados de respuesta de autenticación: Proxy-Authenticate (para la autenticación de proxy) o WWW-Authenticate (para la autenticación del servidor).</span><span class="sxs-lookup"><span data-stu-id="79756-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="79756-111">Cada encabezado de respuesta de autenticación contiene un esquema de autenticación disponible y un dominio kerberos.</span><span class="sxs-lookup"><span data-stu-id="79756-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="79756-112">Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de respuesta de autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="79756-113">El valor de dominio kerberos distingue mayúsculas de minúsculas y define un espacio de protección en el proxy o servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="79756-114">Por ejemplo, el encabezado "WWW-Authenticate: Basic Realm="example" sería un ejemplo de un encabezado devuelto cuando se requiere autenticación de servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="79756-115">La aplicación cliente que envió la solicitud puede autenticarse mediante la inclusión de un campo de encabezado de autorización con la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79756-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="79756-116">El encabezado Authorization contendrá el esquema de autenticación y la respuesta adecuada requerida por ese esquema.</span><span class="sxs-lookup"><span data-stu-id="79756-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="79756-117">Por ejemplo, el encabezado "Authorization: Basic" se agregaría a la solicitud y se volvería a enviar al servidor si el cliente recibió el encabezado de respuesta de autenticación \<username:password> "WWW-Authenticate: Basic Realm="example"".</span><span class="sxs-lookup"><span data-stu-id="79756-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="79756-118">Hay dos tipos generales de esquemas de autenticación:</span><span class="sxs-lookup"><span data-stu-id="79756-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="79756-119">Esquema de autenticación básico, donde el nombre de usuario y la contraseña se envían en texto no cifrado al servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="79756-120">Esquemas de desafío-respuesta, que permiten un formato de desafío-respuesta.</span><span class="sxs-lookup"><span data-stu-id="79756-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="79756-121">El esquema de autenticación básico se basa en el modelo en el que un cliente debe autenticarse con un nombre de usuario y una contraseña para cada dominio.</span><span class="sxs-lookup"><span data-stu-id="79756-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="79756-122">El servidor proporciona servicios a la solicitud si se reenvia con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.</span><span class="sxs-lookup"><span data-stu-id="79756-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="79756-123">Los esquemas de desafío-respuesta permiten una autenticación más segura.</span><span class="sxs-lookup"><span data-stu-id="79756-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="79756-124">Si una solicitud requiere autenticación mediante un esquema de desafío-respuesta, el código de estado adecuado y los encabezados Authenticate se devuelven al cliente.</span><span class="sxs-lookup"><span data-stu-id="79756-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="79756-125">A continuación, el cliente debe volver a enviar la solicitud con una negociación.</span><span class="sxs-lookup"><span data-stu-id="79756-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="79756-126">El servidor devolvería un código de estado adecuado con un desafío y, a continuación, el cliente requeriría volver a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="79756-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="79756-127">En la tabla siguiente se enumeran los esquemas de autenticación, el tipo de autenticación, el archivo DLL que los admite y una descripción del esquema.</span><span class="sxs-lookup"><span data-stu-id="79756-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="79756-128">Scheme</span><span class="sxs-lookup"><span data-stu-id="79756-128">Scheme</span></span>                                    | <span data-ttu-id="79756-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="79756-129">Type</span></span>               | <span data-ttu-id="79756-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79756-130">DLL</span></span>                  | <span data-ttu-id="79756-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="79756-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79756-132">Básico (texto no cifrado)</span><span class="sxs-lookup"><span data-stu-id="79756-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="79756-133">basic</span><span class="sxs-lookup"><span data-stu-id="79756-133">basic</span></span>              | <span data-ttu-id="79756-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="79756-134">Wininet.dll</span></span>          | <span data-ttu-id="79756-135">Usa una cadena codificada en Base64 que contiene el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="79756-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="79756-136">Digest</span><span class="sxs-lookup"><span data-stu-id="79756-136">Digest</span></span>                                    | <span data-ttu-id="79756-137">desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="79756-137">challenge-response</span></span> | <span data-ttu-id="79756-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="79756-138">Digest.dll</span></span>           | <span data-ttu-id="79756-139">Un esquema de desafío-respuesta que se enfrenta al uso de un valor nonce (una cadena de datos especificada por el servidor).</span><span class="sxs-lookup"><span data-stu-id="79756-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="79756-140">Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor nonce especificado, el método HTTP y el identificador uniforme de recursos (URI) solicitado.</span><span class="sxs-lookup"><span data-stu-id="79756-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="79756-141">La compatibilidad con la autenticación implícita se introdujo en Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="79756-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="79756-142">NT LAN Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="79756-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="79756-143">desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="79756-143">challenge-response</span></span> | <span data-ttu-id="79756-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="79756-144">Winsspi.dll</span></span>          | <span data-ttu-id="79756-145">Un esquema de desafío-respuesta que basa el desafío en el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="79756-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="79756-146">Microsoft Network (MSN)</span><span class="sxs-lookup"><span data-stu-id="79756-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="79756-147">desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="79756-147">challenge-response</span></span> | <span data-ttu-id="79756-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="79756-148">Msnsspc.dll</span></span>          | <span data-ttu-id="79756-149">The Microsoft Network esquema de autenticación de .</span><span class="sxs-lookup"><span data-stu-id="79756-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="79756-150">Autenticación con contraseña distribuida (DPA)</span><span class="sxs-lookup"><span data-stu-id="79756-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="79756-151">desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="79756-151">challenge-response</span></span> | <span data-ttu-id="79756-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="79756-152">Msapsspc.dll</span></span>         | <span data-ttu-id="79756-153">Es similar a la autenticación MSN y también lo usa Microsoft Network.</span><span class="sxs-lookup"><span data-stu-id="79756-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="79756-154">Autenticación remota de frase de contraseña (RPA)</span><span class="sxs-lookup"><span data-stu-id="79756-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="79756-155">Compuserve</span><span class="sxs-lookup"><span data-stu-id="79756-155">CompuServe</span></span>         | <span data-ttu-id="79756-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="79756-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="79756-157">Esquema de autenticación de CompuServe.</span><span class="sxs-lookup"><span data-stu-id="79756-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="79756-158">Para obtener más información, vea Especificaciones [del mecanismo de RPA](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="79756-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="79756-159">Para cualquier cosa que no sea la autenticación básica, las claves del Registro deben configurarse además de instalar el archivo DLL adecuado.</span><span class="sxs-lookup"><span data-stu-id="79756-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="79756-160">Si se requiere autenticación, se debe usar la marca [ \_ KEEP \_ \_ CONNECTION](api-flags.md) de INTERNET FLAG en la llamada a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="79756-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="79756-161">La marca KEEP CONNECTION de INTERNET FLAG es necesaria para NTLM y otros tipos de autenticación con el fin de mantener la conexión mientras se \_ completa el proceso de \_ \_ autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="79756-162">Si no se mantiene la conexión, el proceso de autenticación debe reiniciarse con el proxy o el servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="79756-163">Las [**funciones InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completan correctamente incluso cuando se requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="79756-164">La diferencia es que los datos devueltos en los archivos de encabezado e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) recibirían una página HTML que informa al usuario del código de estado.</span><span class="sxs-lookup"><span data-stu-id="79756-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="79756-165">Registro de claves de autenticación</span><span class="sxs-lookup"><span data-stu-id="79756-165">Registering Authentication Keys</span></span>

<span data-ttu-id="79756-166">INTERNET OPEN TYPE PRECONFIG examina los valores del \_ Registro \_ \_ **ProxyEnable,** **ProxyServer** y **ProxyOverride.**</span><span class="sxs-lookup"><span data-stu-id="79756-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="79756-167">Estos valores se encuentran en **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ Windows CurrentVersion Internet Settings (Configuración de Internet de Microsoft **Windows** \\ **CurrentVersion).** \\ </span><span class="sxs-lookup"><span data-stu-id="79756-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="79756-168">Para los esquemas de autenticación distintos de Básico, se debe agregar una clave al Registro en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="79756-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="79756-169">Un **valor DWORD,** **Flags**, debe establecerse con el valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="79756-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="79756-170">En la lista siguiente se muestran los valores posibles para **el valor Flags.**</span><span class="sxs-lookup"><span data-stu-id="79756-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="79756-171">LA \_ AUTENTICACIÓN \_ DEL COMPLEMENTO MARCA UN CONTEXTO ÚNICO POR \_ \_ \_ \_ TCPIP (value=0x01)</span><span class="sxs-lookup"><span data-stu-id="79756-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="79756-172">Cada socket de Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) contiene un contexto diferente.</span><span class="sxs-lookup"><span data-stu-id="79756-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="79756-173">De lo contrario, se pasa un nuevo contexto para cada plantilla de dirección URL de dominio o bloque.</span><span class="sxs-lookup"><span data-stu-id="79756-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="79756-174">LAS \_ MARCAS DE \_ AUTENTICACIÓN DEL COMPLEMENTO PUEDEN CONTROLAR \_ LA INTERFAZ DE USUARIO \_ \_ (value=0x02)</span><span class="sxs-lookup"><span data-stu-id="79756-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="79756-175">Este archivo DLL puede controlar su propia entrada de usuario.</span><span class="sxs-lookup"><span data-stu-id="79756-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="79756-176">LAS \_ MARCAS DE \_ AUTENTICACIÓN DEL COMPLEMENTO PUEDEN CONTROLAR \_ NO \_ \_ \_ PASSWD (value=0x04)</span><span class="sxs-lookup"><span data-stu-id="79756-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="79756-177">Este archivo DLL podría ser capaz de realizar una autenticación sin solicitar al usuario una contraseña.</span><span class="sxs-lookup"><span data-stu-id="79756-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="79756-178">PLUGIN \_ AUTH \_ FLAGS \_ NO REALM \_ (value=0x08)</span><span class="sxs-lookup"><span data-stu-id="79756-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="79756-179">Este archivo DLL no usa una cadena de dominio kerberos HTTP estándar.</span><span class="sxs-lookup"><span data-stu-id="79756-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="79756-180">Los datos que parecen ser un dominio kerberos son datos específicos del esquema.</span><span class="sxs-lookup"><span data-stu-id="79756-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="79756-181">MARCAS \_ DE AUTENTICACIÓN \_ DE COMPLEMENTO KEEP ALIVE NOT REQUIRED \_ \_ \_ \_ (value=0x10)</span><span class="sxs-lookup"><span data-stu-id="79756-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="79756-182">Este archivo DLL no requiere una conexión persistente para su secuencia de desafío-respuesta.</span><span class="sxs-lookup"><span data-stu-id="79756-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="79756-183">Por ejemplo, para agregar la autenticación NTLM, la clave NTLM debe agregarse a **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="79756-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="79756-184">En **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security NTLM , se debe agregar el valor de \\  \\  \\  \\  \\  **cadena, DLLFile** y un **valor DWORD,** **Flags**.</span><span class="sxs-lookup"><span data-stu-id="79756-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="79756-185">**DLLFile** debe establecerse en Winsspi.dll, y **Flags** debe establecerse en 0x08.</span><span class="sxs-lookup"><span data-stu-id="79756-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="79756-186">Autenticación de servidor</span><span class="sxs-lookup"><span data-stu-id="79756-186">Server Authentication</span></span>

<span data-ttu-id="79756-187">Cuando un servidor recibe una solicitud que requiere autenticación, el servidor devuelve un mensaje de código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="79756-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="79756-188">En ese mensaje, el servidor debe incluir uno o varios encabezados WWW-Authenticate respuesta.</span><span class="sxs-lookup"><span data-stu-id="79756-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="79756-189">Estos encabezados incluyen los métodos de autenticación que el servidor tiene disponibles.</span><span class="sxs-lookup"><span data-stu-id="79756-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="79756-190">WinINet elige el primer método que reconoce.</span><span class="sxs-lookup"><span data-stu-id="79756-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="79756-191">La autenticación básica proporciona seguridad débil a menos que el canal se vincule primero con SSL o PCT.</span><span class="sxs-lookup"><span data-stu-id="79756-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="79756-192">La [**función InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada para obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="79756-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="79756-193">Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer los valores [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION \_ \_ USERNAME](option-flags.md) y, a continuación, volver a enviar la solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="79756-194">Autenticación de proxy</span><span class="sxs-lookup"><span data-stu-id="79756-194">Proxy Authentication</span></span>

<span data-ttu-id="79756-195">Cuando un cliente intenta usar un proxy que requiere autenticación, el proxy devuelve un mensaje de código de estado 407 al cliente.</span><span class="sxs-lookup"><span data-stu-id="79756-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="79756-196">En ese mensaje, el proxy debe incluir uno o varios encabezados Proxy-Authenticate respuesta.</span><span class="sxs-lookup"><span data-stu-id="79756-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="79756-197">Estos encabezados incluyen los métodos de autenticación disponibles desde el proxy.</span><span class="sxs-lookup"><span data-stu-id="79756-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="79756-198">WinINet elige el primer método que reconoce.</span><span class="sxs-lookup"><span data-stu-id="79756-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="79756-199">La [**función InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="79756-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="79756-200">Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer los valores INTERNET [OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) y, a continuación, volver a enviar la solicitud al proxy.</span><span class="sxs-lookup"><span data-stu-id="79756-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="79756-201">Si no se establece ningún nombre de usuario y contraseña de proxy, WinINet intenta usar el nombre de usuario y la contraseña para el servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="79756-202">Este comportamiento permite a los clientes implementar la misma interfaz de usuario personalizada que se usa para controlar la autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="79756-203">Control de la autenticación HTTP</span><span class="sxs-lookup"><span data-stu-id="79756-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="79756-204">La autenticación HTTP se puede controlar con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o una función personalizada que usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o agrega sus propios encabezados de autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="79756-205">[**InternetErrorDlg puede examinar**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) los encabezados asociados a un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para buscar errores ocultos, como códigos de estado de un servidor o proxy.</span><span class="sxs-lookup"><span data-stu-id="79756-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="79756-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) se puede usar para establecer el nombre de usuario y la contraseña para el proxy y el servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="79756-207">Para la autenticación de MSN y DPA, [**internetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) debe usarse para establecer el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="79756-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="79756-208">Para cualquier función personalizada que agrega sus propios encabezados WWW-Authenticate o Proxy-Authenticate, la marca [ \_ INTERNET FLAG NO \_ \_ AUTH](api-flags.md) debe establecerse para deshabilitar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="79756-209">En el ejemplo siguiente se muestra cómo se puede usar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) para controlar la autenticación HTTP.</span><span class="sxs-lookup"><span data-stu-id="79756-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="79756-210">En el ejemplo, dwErrorCode se usa para almacenar los errores asociados a la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="79756-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="79756-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completa correctamente, incluso si el servidor o proxy requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="79756-212">Cuando la marca FLAGS ERROR UI FILTER FOR ERRORS se pasa a \_ \_ \_ \_ \_ [**InternetErrorDlg,**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)la función comprueba si hay errores ocultos en los encabezados.</span><span class="sxs-lookup"><span data-stu-id="79756-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="79756-213">Estos errores ocultos incluirían cualquier solicitud de autenticación.</span><span class="sxs-lookup"><span data-stu-id="79756-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="79756-214">[**InternetErrorDlg muestra**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) el cuadro de diálogo adecuado para solicitar al usuario los datos necesarios.</span><span class="sxs-lookup"><span data-stu-id="79756-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="79756-215">Las marcas de interfaz de usuario FLAGS ERROR GENERATE DATA y FLAGS ERROR UI FLAGS CHANGE OPTIONS también se deben pasar a \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)para [](appendix-a-hinternet-handles.md) que la función construya la estructura de datos adecuada para el error y almacena los resultados del cuadro de diálogo en el identificador HINTERNET.</span><span class="sxs-lookup"><span data-stu-id="79756-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="79756-216">En el código de ejemplo siguiente se muestra cómo se puede controlar la autenticación [**mediante InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="79756-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="79756-217">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="79756-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="79756-218">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="79756-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="79756-219">Para implementaciones de servidor o servicios, use [Servicios HTTP de Microsoft Windows (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)</span><span class="sxs-lookup"><span data-stu-id="79756-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 