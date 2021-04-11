---
title: Sesiones HTTP
description: Se tiene acceso a los recursos del WWW mediante http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149386"
---
# <a name="http-sessions"></a><span data-ttu-id="2b3e0-103">Sesiones HTTP</span><span class="sxs-lookup"><span data-stu-id="2b3e0-103">HTTP Sessions</span></span>

<span data-ttu-id="2b3e0-104">WinINet le permite tener acceso a los recursos del World Wide Web (WWW).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="2b3e0-105">Se puede tener acceso a estos recursos directamente mediante [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para obtener más información, vea [acceso directo a las direcciones URL](handling-uniform-resource-locators.md)).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="2b3e0-106">Se tiene acceso a los recursos del WWW mediante http.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="2b3e0-107">Las funciones HTTP controlan los protocolos subyacentes, a la vez que permiten que la aplicación tenga acceso a información en WWW.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="2b3e0-108">A medida que evoluciona el protocolo HTTP, los protocolos subyacentes se actualizan para mantener el comportamiento de la función.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="2b3e0-109">En el diagrama siguiente se muestran las relaciones de las funciones que se utilizan con el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="2b3e0-110">Los cuadros sombreados representan funciones que devuelven los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funciones WinInet utilizadas para http](images/ax-wnt05.png)

<span data-ttu-id="2b3e0-112">Para obtener más información, vea [identificadores de HINTERNET](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="2b3e0-113">Usar las funciones de WinINet para tener acceso a WWW</span><span class="sxs-lookup"><span data-stu-id="2b3e0-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="2b3e0-114">Iniciar una conexión a WWW</span><span class="sxs-lookup"><span data-stu-id="2b3e0-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="2b3e0-115">Abrir una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="2b3e0-116">Agregar encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="2b3e0-117">Envío de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="2b3e0-118">Publicar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="2b3e0-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="2b3e0-119">Obtención de información acerca de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="2b3e0-120">Descargar recursos desde WWW</span><span class="sxs-lookup"><span data-stu-id="2b3e0-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="2b3e0-121">Las siguientes funciones se usan durante las sesiones HTTP para tener acceso a WWW.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="2b3e0-122">Función</span><span class="sxs-lookup"><span data-stu-id="2b3e0-122">Function</span></span>                                               | <span data-ttu-id="2b3e0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b3e0-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b3e0-124">**HttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="2b3e0-125">Agrega encabezados de solicitud HTTP al identificador de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="2b3e0-126">Esta función requiere un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="2b3e0-127">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="2b3e0-128">Abre un identificador de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="2b3e0-129">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="2b3e0-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="2b3e0-131">Consulta información acerca de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="2b3e0-132">Esta función requiere un identificador creado por la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="2b3e0-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="2b3e0-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="2b3e0-134">Envía la solicitud HTTP especificada al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="2b3e0-135">Esta función requiere un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="2b3e0-136">**InternetErrorDlg**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="2b3e0-137">Muestra cuadros de diálogo predefinidos para las condiciones de error comunes de Internet.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="2b3e0-138">Esta función requiere el identificador usado en la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="2b3e0-139">Iniciar una conexión a WWW</span><span class="sxs-lookup"><span data-stu-id="2b3e0-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="2b3e0-140">Para iniciar una conexión a WWW, la aplicación debe llamar a la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en el [**HINTERNET**](appendix-a-hinternet-handles.md) raíz devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="2b3e0-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe establecer una sesión http declarando el \_ tipo de servicio http del servicio de Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="2b3e0-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="2b3e0-142">Para obtener más información sobre el uso de [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consulte [uso de InternetConnect](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="2b3e0-143">Abrir una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-143">Opening a Request</span></span>

<span data-ttu-id="2b3e0-144">La función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abre una solicitud HTTP y devuelve un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que pueden usar las otras funciones http.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="2b3e0-145">A diferencia de las otras funciones abiertas (como [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) no envía la solicitud a Internet cuando se llama.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="2b3e0-146">La función [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud y establece una conexión a través de la red.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="2b3e0-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) toma un identificador de sesión http creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y un verbo http, un nombre de objeto, una cadena de versión, un referrer, tipos de aceptación, marcas y valores de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="2b3e0-148">El verbo HTTP es una cadena que se va a usar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="2b3e0-149">Los verbos HTTP comunes que se usan en las solicitudes incluyen GET, PUT y POST.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="2b3e0-150">Si este valor se establece en **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa el valor predeterminado get.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="2b3e0-151">El nombre del objeto es una cadena que contiene el nombre del objeto de destino del verbo HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="2b3e0-152">Suele ser un nombre de archivo, un módulo ejecutable o un especificador de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="2b3e0-153">Si el nombre de objeto proporcionado es una cadena vacía, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) busca la página predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="2b3e0-154">La cadena de versión debe contener la versión HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="2b3e0-155">Si este parámetro es **null**, la función utiliza "" http/1.1 "".</span><span class="sxs-lookup"><span data-stu-id="2b3e0-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="2b3e0-156">El remitente de referencia especifica la dirección del documento a partir del que se obtuvo el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="2b3e0-157">Si este parámetro es **null**, no se especifica ningún referencia.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="2b3e0-158">La cadena terminada en **null** que contiene los tipos de aceptación indica los tipos de contenido aceptados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="2b3e0-159">Establecer este parámetro en **null** indica que la aplicación no acepta ningún tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="2b3e0-160">Si se proporciona una cadena vacía, la aplicación indica que solo acepta documentos de tipo "" Text/ \* "".</span><span class="sxs-lookup"><span data-stu-id="2b3e0-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="2b3e0-161">El valor "" Text/ \* "" indica documentos solo de texto, no imágenes u otros archivos binarios.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="2b3e0-162">Los valores de marca controlan el almacenamiento en caché, las cookies y los problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="2b3e0-163">En el caso de Microsoft Network (MSN), NTLM y otros tipos de autenticación, establezca la marca de [Internet \_ marcar para mantener la \_ \_ conexión](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="2b3e0-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="2b3e0-164">Si se estableció la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), debe establecerse un valor de contexto distinto de cero para la operación asincrónica correcta.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="2b3e0-165">En el ejemplo siguiente se muestra una llamada de ejemplo a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="2b3e0-166">Agregar encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-166">Adding Request Headers</span></span>

<span data-ttu-id="2b3e0-167">La función [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permite que las aplicaciones agreguen uno o más encabezados de solicitud a la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="2b3e0-168">Esta función permite a una aplicación anexar encabezados de formato libre adicionales al identificador de la solicitud HTTP; está diseñado para aplicaciones sofisticadas que requieren un control preciso de la solicitud enviada al servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="2b3e0-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) necesita un identificador de solicitud HTTP creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), una cadena que contiene los encabezados, la longitud de los encabezados y los modificadores.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="2b3e0-170">Envío de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-170">Sending a Request</span></span>

<span data-ttu-id="2b3e0-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establece una conexión a Internet y envía la solicitud al sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="2b3e0-172">Esta función requiere un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="2b3e0-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) también puede enviar encabezados adicionales u información opcional.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="2b3e0-174">La información opcional se utiliza generalmente para las operaciones que escriben información en el servidor, como PUT y POST.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="2b3e0-175">Una vez que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud, la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) en el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) para descargar los recursos del servidor.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="2b3e0-176">Publicar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="2b3e0-176">Posting Data to the Server</span></span>

<span data-ttu-id="2b3e0-177">Para publicar datos en un servidor, el verbo HTTP de la llamada a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) debe ser post o Put.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="2b3e0-178">La dirección del búfer que contiene los datos de envío se debe pasar al parámetro *lpOptional* en [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="2b3e0-179">El parámetro *dwOptionalLength* debe establecerse en el tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="2b3e0-180">También puede usar la función [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para publicar datos en un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) enviado mediante [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="2b3e0-181">Obtención de información acerca de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2b3e0-181">Getting Information About a Request</span></span>

<span data-ttu-id="2b3e0-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permite que una aplicación recupere información acerca de una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="2b3e0-183">La función requiere un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), un valor de nivel de información y una longitud de búfer.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="2b3e0-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) también acepta un búfer que almacena la información y un índice de encabezado basado en cero que enumera varios encabezados con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="2b3e0-185">Descargar recursos desde WWW</span><span class="sxs-lookup"><span data-stu-id="2b3e0-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="2b3e0-186">Después de abrir una solicitud con [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviarla al servidor con [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) para descargar el recurso desde el servidor http.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="2b3e0-187">En el ejemplo siguiente se descarga un recurso.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-187">The following example downloads a resource.</span></span> <span data-ttu-id="2b3e0-188">La función acepta el identificador de la ventana actual, el número de identificación de un cuadro de edición y un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="2b3e0-189">Usa [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) para determinar el tamaño del recurso y luego lo descarga mediante [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="2b3e0-190">El contenido se muestra en el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="2b3e0-191">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="2b3e0-192">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2b3e0-193">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 