---
title: Cookies HTTP
description: Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704977"
---
# <a name="http-cookies"></a><span data-ttu-id="4b893-103">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="4b893-103">HTTP Cookies</span></span>

<span data-ttu-id="4b893-104">Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4b893-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="4b893-105">Este mecanismo permite a las aplicaciones basadas en Web almacenar información sobre los elementos seleccionados, las preferencias del usuario, la información de registro y otra información que se puede recuperar más adelante.</span><span class="sxs-lookup"><span data-stu-id="4b893-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="4b893-106">Encabezados de Cookie-Related</span><span class="sxs-lookup"><span data-stu-id="4b893-106">Cookie-Related Headers</span></span>

<span data-ttu-id="4b893-107">Hay dos encabezados, Set-Cookie y cookie, que están relacionados con las cookies.</span><span class="sxs-lookup"><span data-stu-id="4b893-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="4b893-108">El servidor envía el encabezado Set-Cookie como respuesta a una solicitud HTTP, que se usa para crear una cookie en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b893-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="4b893-109">La aplicación cliente incluye el encabezado de la cookie con una solicitud HTTP enviada a un servidor, si hay una cookie que tenga un dominio y una ruta de acceso coincidentes.</span><span class="sxs-lookup"><span data-stu-id="4b893-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="4b893-110">Encabezado Set-Cookie</span><span class="sxs-lookup"><span data-stu-id="4b893-110">Set-Cookie Header</span></span>

<span data-ttu-id="4b893-111">El encabezado de respuesta Set-Cookie utiliza el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b893-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="4b893-112"> = En el encabezado de respuesta Set-Cookie se deben incluir una o varias secuencias de cadenas (separadas por punto y coma) que sigan el *valor* del nombre del patrón.</span><span class="sxs-lookup"><span data-stu-id="4b893-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="4b893-113">El servidor puede utilizar estas secuencias de cadenas para almacenar datos en el sistema del cliente.</span><span class="sxs-lookup"><span data-stu-id="4b893-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="4b893-114">La fecha de expiración se establece mediante el formato Expires =*Date*, donde *Date* es la fecha de expiración en la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="4b893-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="4b893-115">Si no se establece la fecha de expiración, la cookie expira una vez finalizada la sesión de Internet.</span><span class="sxs-lookup"><span data-stu-id="4b893-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="4b893-116">De lo contrario, la cookie se conserva en la memoria caché hasta la fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="4b893-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="4b893-117">La fecha debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b893-117">The date must use the following format:</span></span>

<span data-ttu-id="4b893-118">*día*, *DD* - *MMM* - *AAAA* *HH*:*mm*:*SS* GMT</span><span class="sxs-lookup"><span data-stu-id="4b893-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="4b893-119"><span id="DAY"></span><span id="day"></span>*DIARIAMENTE*</span><span class="sxs-lookup"><span data-stu-id="4b893-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-120">El día de la semana (sol, Lun, mar, Mié, Jue, Vie, SAT).</span><span class="sxs-lookup"><span data-stu-id="4b893-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="4b893-121"><span id="DD"></span><span id="dd"></span>*DD*</span><span class="sxs-lookup"><span data-stu-id="4b893-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-122">Día del mes (por ejemplo, 01 para el primer día del mes).</span><span class="sxs-lookup"><span data-stu-id="4b893-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="4b893-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span><span class="sxs-lookup"><span data-stu-id="4b893-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-124">La abreviatura de tres letras para el mes (Jan, Feb, mar, Apr, mayo, Jun, Jul, ago, Sep, Oct, Nov, DEC).</span><span class="sxs-lookup"><span data-stu-id="4b893-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="4b893-125"><span id="YYYY"></span><span id="yyyy"></span>*AAA*</span><span class="sxs-lookup"><span data-stu-id="4b893-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-126">Año.</span><span class="sxs-lookup"><span data-stu-id="4b893-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="4b893-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="4b893-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-128">El valor de hora en hora militar (22 sería de 10:00 P.M., por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="4b893-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="4b893-129"><span id="MM"></span><span id="mm"></span>*MM*</span><span class="sxs-lookup"><span data-stu-id="4b893-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-130">Valor del minuto.</span><span class="sxs-lookup"><span data-stu-id="4b893-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="4b893-131"><span id="SS"></span><span id="ss"></span>*SS*</span><span class="sxs-lookup"><span data-stu-id="4b893-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="4b893-132">Segundo valor.</span><span class="sxs-lookup"><span data-stu-id="4b893-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="4b893-133">Especificar el nombre de dominio, con el patrón domain =*\_ nombre de dominio*, es opcional para las cookies persistentes y se usa para indicar el final del dominio para el que la cookie es válida.</span><span class="sxs-lookup"><span data-stu-id="4b893-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="4b893-134">Se rechazan las cookies de sesión que especifican un dominio.</span><span class="sxs-lookup"><span data-stu-id="4b893-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="4b893-135">Si el nombre de dominio especificado finaliza con la solicitud, la cookie intenta coincidir con la ruta de acceso para determinar si se debe enviar la cookie.</span><span class="sxs-lookup"><span data-stu-id="4b893-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="4b893-136">Por ejemplo, si el nombre de dominio final es. microsoft.com, las solicitudes a home.microsoft.com y support.microsoft.com se comprueban para ver si el patrón especificado coincide con la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b893-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="4b893-137">El nombre de dominio debe tener al menos dos o tres períodos para evitar que las cookies se establezcan para los finales de nombres de dominio ampliamente utilizados, como. com,. edu y co.jp.</span><span class="sxs-lookup"><span data-stu-id="4b893-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="4b893-138">Los nombres de dominio permitidos serían similares a. microsoft.com,. someschool.edu y. someserver.co.jp.</span><span class="sxs-lookup"><span data-stu-id="4b893-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="4b893-139">Solo los hosts dentro del dominio especificado pueden establecer una cookie para un dominio.</span><span class="sxs-lookup"><span data-stu-id="4b893-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="4b893-140">La configuración de la ruta de acceso, mediante la ruta de acceso del patrón =*some \_*, es opcional y se puede usar para especificar un subconjunto de las direcciones URL para las que la cookie es válida.</span><span class="sxs-lookup"><span data-stu-id="4b893-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="4b893-141">Si se especifica una ruta de acceso, la cookie se considera válida para las solicitudes que coinciden con dicha ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4b893-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="4b893-142">Por ejemplo, si la ruta de acceso especificada es/example, las solicitudes con las rutas de acceso/examplecode y/example/code.htm coincidirán.</span><span class="sxs-lookup"><span data-stu-id="4b893-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="4b893-143">Si no se especifica ninguna ruta de acceso, se supone que la ruta de acceso es la ruta de acceso del recurso asociado al encabezado Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="4b893-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="4b893-144">La cookie también se puede marcar como segura, lo que especifica que la cookie solo se puede enviar a servidores https.</span><span class="sxs-lookup"><span data-stu-id="4b893-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="4b893-145">Por último, una cookie se puede marcar como HttpOnly (los atributos no distinguen mayúsculas de minúsculas) para indicar que la cookie no admite scripts y no debe revelarse a la aplicación cliente por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4b893-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="4b893-146">Dentro de Windows Internet, esto significa que no se puede recuperar la cookie a través de la función **InternetGetCookie** .</span><span class="sxs-lookup"><span data-stu-id="4b893-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="4b893-147">Encabezado de cookie</span><span class="sxs-lookup"><span data-stu-id="4b893-147">Cookie Header</span></span>

<span data-ttu-id="4b893-148">El encabezado de la cookie se incluye con todas las solicitudes HTTP que tienen una cookie cuyo dominio y ruta de acceso coinciden con la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b893-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="4b893-149">El encabezado de la cookie tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="4b893-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="4b893-150">Una o varias secuencias de cadenas, utilizando el valor de *nombre* de formato = , contienen la información que se estableció en la cookie.</span><span class="sxs-lookup"><span data-stu-id="4b893-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="4b893-151">Generar cookies</span><span class="sxs-lookup"><span data-stu-id="4b893-151">Generating Cookies</span></span>

<span data-ttu-id="4b893-152">Existen tres métodos para generar cookies para Microsoft Internet Explorer: usar Microsoft JScript, usar las funciones de WinINet y usar un script CGI.</span><span class="sxs-lookup"><span data-stu-id="4b893-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="4b893-153">Todos los métodos deben establecer la información que se incluye en el encabezado de Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="4b893-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="4b893-154">Generar una cookie mediante el modelo de objetos DHTML</span><span class="sxs-lookup"><span data-stu-id="4b893-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="4b893-155">Con el modelo de objetos de HTML dinámico (DHTML), las cookies se pueden establecer mediante una llamada a la propiedad **Cookie** del objeto de documento, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b893-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="4b893-156">Generar una cookie mediante las funciones WinInet</span><span class="sxs-lookup"><span data-stu-id="4b893-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="4b893-157">Las aplicaciones pueden crear cookies mediante la función [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="4b893-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="4b893-158">Para obtener más información, consulte [configuración de una cookie](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="4b893-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="4b893-159">Generación de una cookie mediante un script CGI</span><span class="sxs-lookup"><span data-stu-id="4b893-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="4b893-160">Las cookies se generan mediante la inclusión de un encabezado Set-Cookie como parte de un script CGI incluido en la respuesta HTTP a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b893-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="4b893-161">El ejemplo siguiente es un script CGI que incluye un encabezado Set-Cookie mediante Perl.</span><span class="sxs-lookup"><span data-stu-id="4b893-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="4b893-162">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="4b893-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="4b893-163">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="4b893-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="4b893-164">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="4b893-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 