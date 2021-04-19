---
description: Algunos servidores HTTP y servidores proxy requieren autenticación antes de permitir el acceso a los recursos en Internet. Las funciones de servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para sesiones HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticación en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380831"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="00d8c-104">Autenticación en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00d8c-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="00d8c-105">Algunos servidores HTTP y servidores proxy requieren autenticación antes de permitir el acceso a los recursos en Internet.</span><span class="sxs-lookup"><span data-stu-id="00d8c-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="00d8c-106">Las funciones de servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para sesiones HTTP.</span><span class="sxs-lookup"><span data-stu-id="00d8c-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="00d8c-107">Acerca de la autenticación HTTP</span><span class="sxs-lookup"><span data-stu-id="00d8c-107">About HTTP Authentication</span></span>

<span data-ttu-id="00d8c-108">Si se requiere autenticación, la aplicación HTTP recibe un código de estado 401 (el servidor requiere autenticación) o 407 (el proxy requiere autenticación).</span><span class="sxs-lookup"><span data-stu-id="00d8c-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="00d8c-109">Junto con el código de estado, el servidor o proxy envía uno o varios encabezados de autenticación: WWW-Authenticate (para la autenticación del servidor) o Proxy-Authenticate (para la autenticación de proxy).</span><span class="sxs-lookup"><span data-stu-id="00d8c-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="00d8c-110">Cada encabezado de autenticación contiene un esquema de autenticación compatible y, para los esquemas Básico e Implícita, un dominio kerberos.</span><span class="sxs-lookup"><span data-stu-id="00d8c-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="00d8c-111">Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="00d8c-112">El valor de dominio kerberos distingue mayúsculas de minúsculas y define un conjunto de servidores o servidores proxy para los que se aceptan las mismas credenciales.</span><span class="sxs-lookup"><span data-stu-id="00d8c-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="00d8c-113">Por ejemplo, el encabezado "WWW-Authenticate: Basic Realm="example" podría devolverse cuando se requiere la autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="00d8c-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="00d8c-114">Este encabezado especifica que se deben proporcionar credenciales de usuario para el dominio "ejemplo".</span><span class="sxs-lookup"><span data-stu-id="00d8c-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="00d8c-115">Una aplicación HTTP puede incluir un campo de encabezado de autorización con una solicitud que envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="00d8c-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="00d8c-116">El encabezado de autorización contiene el esquema de autenticación y la respuesta adecuada requerida por ese esquema.</span><span class="sxs-lookup"><span data-stu-id="00d8c-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="00d8c-117">Por ejemplo, el encabezado "Authorization: Basic" se agregaría a la solicitud y se enviaría al servidor si el cliente recibió el encabezado de respuesta \<username:password> "WWW-Authenticate: Basic Realm="example"".</span><span class="sxs-lookup"><span data-stu-id="00d8c-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="00d8c-118">Aunque se muestran aquí como texto sin formato, el nombre de usuario y la contraseña están [*codificados en base64.*](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="00d8c-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="00d8c-119">Hay dos tipos generales de esquemas de autenticación:</span><span class="sxs-lookup"><span data-stu-id="00d8c-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="00d8c-120">Esquema de autenticación básico, en el que el nombre de usuario y la contraseña se envían sin formato al servidor.</span><span class="sxs-lookup"><span data-stu-id="00d8c-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="00d8c-121">El esquema de autenticación básica se basa en el modelo que un cliente debe identificarse con un nombre de usuario y una contraseña para cada dominio.</span><span class="sxs-lookup"><span data-stu-id="00d8c-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="00d8c-122">El servidor solo proporciona servicios a la solicitud si la solicitud se envía con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.</span><span class="sxs-lookup"><span data-stu-id="00d8c-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="00d8c-123">Esquemas de desafío-respuesta, como Kerberos, en los que el servidor reta al cliente con datos [*de autenticación*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="00d8c-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="00d8c-124">El cliente transforma los datos con las credenciales de usuario y envía los datos transformados de vuelta al servidor para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="00d8c-125">Los esquemas de desafío-respuesta permiten una autenticación más segura.</span><span class="sxs-lookup"><span data-stu-id="00d8c-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="00d8c-126">En un esquema de desafío-respuesta, el nombre de usuario y la contraseña nunca se transmiten a través de la red.</span><span class="sxs-lookup"><span data-stu-id="00d8c-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="00d8c-127">Una vez que el cliente selecciona un esquema de desafío-respuesta, el servidor devuelve un código de estado adecuado con un desafío que contiene los datos de [*autenticación*](glossary.md) para ese esquema.</span><span class="sxs-lookup"><span data-stu-id="00d8c-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="00d8c-128">A continuación, el cliente vuelve a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="00d8c-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="00d8c-129">Los esquemas de desafío-respuesta pueden tardar varios intercambios en completarse.</span><span class="sxs-lookup"><span data-stu-id="00d8c-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="00d8c-130">La tabla siguiente contiene los esquemas de autenticación admitidos por WinHTTP, el tipo de autenticación y una descripción del esquema.</span><span class="sxs-lookup"><span data-stu-id="00d8c-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="00d8c-131">Scheme</span><span class="sxs-lookup"><span data-stu-id="00d8c-131">Scheme</span></span>            | <span data-ttu-id="00d8c-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="00d8c-132">Type</span></span>               | <span data-ttu-id="00d8c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="00d8c-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d8c-134">Básico (texto no cifrado)</span><span class="sxs-lookup"><span data-stu-id="00d8c-134">Basic (plaintext)</span></span> | <span data-ttu-id="00d8c-135">Básico</span><span class="sxs-lookup"><span data-stu-id="00d8c-135">Basic</span></span>              | <span data-ttu-id="00d8c-136">Usa una [*cadena codificada en base64*](glossary.md) que contiene el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="00d8c-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="00d8c-137">Digest</span><span class="sxs-lookup"><span data-stu-id="00d8c-137">Digest</span></span>            | <span data-ttu-id="00d8c-138">Desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="00d8c-138">Challenge-response</span></span> | <span data-ttu-id="00d8c-139">Desafíos al usar un valor nonce (una cadena de datos especificada por el servidor).</span><span class="sxs-lookup"><span data-stu-id="00d8c-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="00d8c-140">Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor nonce especificado, el verbo [*HTTP*](glossary.md)y el identificador uniforme de recursos (URI) solicitado.</span><span class="sxs-lookup"><span data-stu-id="00d8c-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="00d8c-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="00d8c-141">NTLM</span></span>              | <span data-ttu-id="00d8c-142">Desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="00d8c-142">Challenge-response</span></span> | <span data-ttu-id="00d8c-143">Requiere que los [*datos de autenticación*](glossary.md) se transformen con las credenciales de usuario para demostrar la identidad.</span><span class="sxs-lookup"><span data-stu-id="00d8c-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="00d8c-144">Para que la autenticación NTLM funcione correctamente, deben realizarse varios intercambios en la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="00d8c-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="00d8c-145">Por lo tanto, no se puede usar la autenticación NTLM si un proxy que interviene no admite conexiones keep-alive.</span><span class="sxs-lookup"><span data-stu-id="00d8c-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="00d8c-146">También se produce un error en la autenticación NTLM si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que deshabilita la semántica de keep-alive.</span><span class="sxs-lookup"><span data-stu-id="00d8c-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="00d8c-147">Passport</span><span class="sxs-lookup"><span data-stu-id="00d8c-147">Passport</span></span>          | <span data-ttu-id="00d8c-148">Desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="00d8c-148">Challenge-response</span></span> | <span data-ttu-id="00d8c-149">Usa [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="00d8c-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="00d8c-150">Negotiate</span><span class="sxs-lookup"><span data-stu-id="00d8c-150">Negotiate</span></span>         | <span data-ttu-id="00d8c-151">Desafío-respuesta</span><span class="sxs-lookup"><span data-stu-id="00d8c-151">Challenge-response</span></span> | <span data-ttu-id="00d8c-152">Si el servidor y el cliente usan Windows 2000 o posterior, se usa la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="00d8c-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="00d8c-153">De lo contrario, se usa la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="00d8c-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="00d8c-154">Kerberos está disponible en sistemas operativos Windows 2000 y versiones posteriores y se considera más seguro que la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="00d8c-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="00d8c-155">Para que la autenticación Negotiate funcione correctamente, deben realizarse varios intercambios en la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="00d8c-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="00d8c-156">Por lo tanto, no se puede usar la autenticación Negotiate si un proxy que interviene no admite conexiones de conexión continua.</span><span class="sxs-lookup"><span data-stu-id="00d8c-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="00d8c-157">La autenticación negotiate también produce un error si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que deshabilita la semántica de conexión continua.</span><span class="sxs-lookup"><span data-stu-id="00d8c-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="00d8c-158">El esquema de autenticación Negotiate a veces se denomina Integrated autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="00d8c-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="00d8c-159">Autenticación en aplicaciones WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00d8c-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="00d8c-160">La interfaz de programación de aplicaciones (API) WinHTTP proporciona dos funciones que se usan para acceder a los recursos de Internet en situaciones en las que se requiere autenticación: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) y [**WinHttpQueryAuthSchemes.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)</span><span class="sxs-lookup"><span data-stu-id="00d8c-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="00d8c-161">Cuando se recibe una respuesta con un código de estado 401 o 407, Se puede usar [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para analizar los encabezados de autenticación para determinar los esquemas de autenticación admitidos y el destino de autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="00d8c-162">El destino de autenticación es el servidor o proxy que solicita la autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="00d8c-163">**WinHttpQueryAuthSchemes** también determina el primer esquema de autenticación, a partir de los esquemas disponibles, en función de las preferencias de esquema de autenticación sugeridas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="00d8c-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="00d8c-164">Este método para elegir un esquema de autenticación es el comportamiento sugerido por [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="00d8c-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="00d8c-165">[**WinHttpSetCredentials permite**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) a una aplicación especificar el esquema de autenticación que se usa junto con un nombre de usuario y una contraseña válidos para su uso en el servidor o proxy de destino.</span><span class="sxs-lookup"><span data-stu-id="00d8c-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="00d8c-166">Después de establecer las credenciales y volver a enviar la solicitud, los encabezados necesarios se generan y se agregan a la solicitud automáticamente.</span><span class="sxs-lookup"><span data-stu-id="00d8c-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="00d8c-167">Dado que algunos esquemas de autenticación requieren varias [**transacciones, WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) podría devolver el error, ERROR \_ WINHTTP \_ RESEND \_ REQUEST.</span><span class="sxs-lookup"><span data-stu-id="00d8c-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="00d8c-168">Cuando se produce este error, la aplicación debe seguir reenendiendo la solicitud hasta que se reciba una respuesta que no contenga un código de estado 401 o 407.</span><span class="sxs-lookup"><span data-stu-id="00d8c-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="00d8c-169">Un código de estado 200 indica que el recurso está disponible y la solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="00d8c-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="00d8c-170">Consulte [**Códigos de estado HTTP para**](http-status-codes.md) obtener códigos de estado adicionales que se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="00d8c-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="00d8c-171">Si se conocen un esquema de autenticación aceptable y las credenciales antes de enviar una solicitud al servidor, una aplicación puede llamar a [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) antes de llamar a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="00d8c-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="00d8c-172">En este caso, WinHTTP intenta la autenticación [](glossary.md) previa con el servidor proporcionando credenciales o datos de autenticación en la solicitud inicial al servidor.</span><span class="sxs-lookup"><span data-stu-id="00d8c-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="00d8c-173">La autenticación previa puede reducir el número de intercambios en el proceso de autenticación y, por tanto, mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="00d8c-174">La autenticación previa se puede usar con los siguientes esquemas de autenticación:</span><span class="sxs-lookup"><span data-stu-id="00d8c-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="00d8c-175">Básico: siempre es posible.</span><span class="sxs-lookup"><span data-stu-id="00d8c-175">Basic - always possible.</span></span>
-   <span data-ttu-id="00d8c-176">Negociación de la resolución en Kerberos: es muy probable que sea posible. la única excepción es cuando los sesgos de tiempo están desactivados entre el cliente y el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="00d8c-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="00d8c-177">(Negociar la resolución en NTLM): nunca es posible.</span><span class="sxs-lookup"><span data-stu-id="00d8c-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="00d8c-178">NTLM: solo es posible en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="00d8c-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="00d8c-179">Implícita: nunca es posible.</span><span class="sxs-lookup"><span data-stu-id="00d8c-179">Digest - never possible.</span></span>
-   <span data-ttu-id="00d8c-180">Passport: nunca es posible; después del desafío-respuesta inicial, WinHTTP usa cookies para autenticarse previamente en Passport.</span><span class="sxs-lookup"><span data-stu-id="00d8c-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="00d8c-181">Una aplicación WinHTTP típica completa los pasos siguientes para controlar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="00d8c-182">Solicite un recurso con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) y [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="00d8c-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="00d8c-183">Compruebe los encabezados de respuesta [**con WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)</span><span class="sxs-lookup"><span data-stu-id="00d8c-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="00d8c-184">Si se devuelve un código de estado 401 o 407 que indica que se requiere autenticación, llame a [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para encontrar un esquema aceptable.</span><span class="sxs-lookup"><span data-stu-id="00d8c-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="00d8c-185">Establezca el esquema de autenticación, el nombre de usuario y la contraseña [**con WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)</span><span class="sxs-lookup"><span data-stu-id="00d8c-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="00d8c-186">Vuelva a enviar la solicitud con el mismo identificador de solicitud mediante una llamada [**a WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="00d8c-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="00d8c-187">Las credenciales establecidas [**por WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) solo se usan para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="00d8c-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="00d8c-188">WinHTTP no almacena en caché las credenciales que se usarán en otras solicitudes, lo que significa que se deben escribir aplicaciones que puedan responder a varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="00d8c-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="00d8c-189">Si se vuelve a usar una conexión autenticada, es posible que no se reta a otras solicitudes, pero el código debe poder responder a una solicitud en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="00d8c-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="00d8c-190">Ejemplo: Recuperar un documento</span><span class="sxs-lookup"><span data-stu-id="00d8c-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="00d8c-191">El código de ejemplo siguiente intenta recuperar un documento especificado de un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="00d8c-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="00d8c-192">El código de estado se recupera de la respuesta para determinar si se requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="00d8c-193">Si se encuentra un código de estado 200, el documento está disponible.</span><span class="sxs-lookup"><span data-stu-id="00d8c-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="00d8c-194">Si se encuentra un código de estado 401 o 407, se requiere autenticación para poder recuperar el documento.</span><span class="sxs-lookup"><span data-stu-id="00d8c-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="00d8c-195">Para cualquier otro código de estado, se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="00d8c-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="00d8c-196">Consulte [**Códigos de estado HTTP**](http-status-codes.md) para obtener una lista de posibles códigos de estado.</span><span class="sxs-lookup"><span data-stu-id="00d8c-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="00d8c-197">Directiva de inicio de sesión automático</span><span class="sxs-lookup"><span data-stu-id="00d8c-197">Automatic Logon Policy</span></span>

<span data-ttu-id="00d8c-198">La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="00d8c-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="00d8c-199">Las credenciales predeterminadas son el token de subproceso actual o el token de sesión en función de si WinHTTP se usa en modo sincrónico o asincrónico.</span><span class="sxs-lookup"><span data-stu-id="00d8c-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="00d8c-200">El token de subproceso se usa en modo sincrónico y el token de sesión se usa en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="00d8c-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="00d8c-201">Estas credenciales predeterminadas suelen ser el nombre de usuario y la contraseña que se usan para iniciar sesión en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="00d8c-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="00d8c-202">La directiva de inicio de sesión automático se implementó para evitar que estas credenciales se usaran ocasionalmente para autenticarse en un servidor que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="00d8c-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="00d8c-203">De forma predeterminada, el nivel de seguridad se establece en WINHTTP \_ AUTOLOGON SECURITY LEVEL MEDIUM, lo que permite usar las credenciales predeterminadas solo para las solicitudes \_ \_ de \_ intranet.</span><span class="sxs-lookup"><span data-stu-id="00d8c-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="00d8c-204">La directiva de inicio de sesión automático solo se aplica a los esquemas de autenticación NTLM y Negotiate.</span><span class="sxs-lookup"><span data-stu-id="00d8c-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="00d8c-205">Las credenciales nunca se transmiten automáticamente con otros esquemas.</span><span class="sxs-lookup"><span data-stu-id="00d8c-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="00d8c-206">La directiva de inicio de sesión automático se puede establecer mediante la [**función WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la [**marca WINHTTP OPTION \_ \_ AUTOLOGON \_ POLICY.**](option-flags.md)</span><span class="sxs-lookup"><span data-stu-id="00d8c-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="00d8c-207">Esta marca solo se aplica al identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="00d8c-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="00d8c-208">Cuando la directiva se establece en WINHTTP AUTOLOGON SECURITY LEVEL LOW, las credenciales predeterminadas se pueden \_ enviar a todos los \_ \_ \_ servidores.</span><span class="sxs-lookup"><span data-stu-id="00d8c-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="00d8c-209">Cuando la directiva se establece en WINHTTP AUTOLOGON SECURITY LEVEL HIGH, las credenciales predeterminadas \_ no se pueden usar para la \_ \_ \_ autenticación.</span><span class="sxs-lookup"><span data-stu-id="00d8c-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="00d8c-210">Se recomienda encarecidamente usar el inicio de sesión automático en el nivel MEDIO.</span><span class="sxs-lookup"><span data-stu-id="00d8c-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="00d8c-211">Nombres de usuarios y contraseñas almacenados</span><span class="sxs-lookup"><span data-stu-id="00d8c-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="00d8c-212">Windows XP introdujo el concepto de nombres de usuario y contraseñas almacenados.</span><span class="sxs-lookup"><span data-stu-id="00d8c-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="00d8c-213">Si las credenciales de Passport de un usuario se guardan mediante el Asistente para registro de **Passport** o el cuadro de diálogo de credenciales estándar **,** se guarda en los nombres de usuario y contraseñas almacenados.</span><span class="sxs-lookup"><span data-stu-id="00d8c-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="00d8c-214">Cuando se usa WinHTTP en Windows XP o versiones posteriores, WinHTTP usa automáticamente las credenciales de los nombres de usuario almacenados y contraseñas si las credenciales no se establecen explícitamente.</span><span class="sxs-lookup"><span data-stu-id="00d8c-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="00d8c-215">Esto es similar a la compatibilidad con las credenciales de inicio de sesión predeterminadas para NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="00d8c-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="00d8c-216">Sin embargo, el uso de credenciales predeterminadas de Passport no está sujeto a la configuración de la directiva de inicio de sesión automático.</span><span class="sxs-lookup"><span data-stu-id="00d8c-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



