---
title: Administrar cookies
description: En el protocolo http, un servidor o un script utiliza cookies para mantener la información de estado en la estación de trabajo cliente.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656375"
---
# <a name="managing-cookies"></a><span data-ttu-id="f2d54-103">Administrar cookies</span><span class="sxs-lookup"><span data-stu-id="f2d54-103">Managing Cookies</span></span>

<span data-ttu-id="f2d54-104">En el protocolo http, un servidor o un script utiliza cookies para mantener la información de estado en la estación de trabajo cliente.</span><span class="sxs-lookup"><span data-stu-id="f2d54-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="f2d54-105">Las funciones WinINet han implementado una base de datos de cookies persistente para este fin.</span><span class="sxs-lookup"><span data-stu-id="f2d54-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="f2d54-106">Se pueden usar para establecer cookies en y obtener acceso a las cookies desde la base de datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="f2d54-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="f2d54-107">Para obtener más información, vea [cookies http](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="f2d54-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="f2d54-108">Las funciones [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) y [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) se pueden usar para administrar cookies.</span><span class="sxs-lookup"><span data-stu-id="f2d54-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="f2d54-109">Usar funciones de cookie</span><span class="sxs-lookup"><span data-stu-id="f2d54-109">Using Cookie Functions</span></span>

<span data-ttu-id="f2d54-110">Las funciones siguientes permiten a una aplicación crear o recuperar cookies en la base de datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="f2d54-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="f2d54-111">Función</span><span class="sxs-lookup"><span data-stu-id="f2d54-111">Function</span></span>                                       | <span data-ttu-id="f2d54-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2d54-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f2d54-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="f2d54-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="f2d54-114">Recupera las cookies para la dirección URL especificada y todas sus direcciones URL primarias.</span><span class="sxs-lookup"><span data-stu-id="f2d54-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="f2d54-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="f2d54-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="f2d54-116">Establece una cookie en la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="f2d54-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="f2d54-117">Tenga en cuenta que estas funciones no requieren una llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="f2d54-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="f2d54-118">Las cookies que tienen una fecha de expiración se almacenan en la cuenta de usuarios locales en el directorio de usuarios \\ "nombre de usuario" \\ AppData \\ roaming de \\ Microsoft \\ Windows \\ cookies y el nombre de usuario \\ "nombreusuario" \\ AppData \\ itinerancia \\ \\ de Microsoft Windows \\ cookies \\ Low Directory para las aplicaciones que se ejecutan con pocos privilegios.</span><span class="sxs-lookup"><span data-stu-id="f2d54-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="f2d54-119">Las cookies que no tienen una fecha de expiración se almacenan en memoria y solo están disponibles para el proceso en el que se crearon.</span><span class="sxs-lookup"><span data-stu-id="f2d54-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="f2d54-120">Como se indica en el tema [cookies http](http-cookies.md) , la función [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) no devuelve las cookies marcadas por el servidor como no Scriptable con el atributo "HttpOnly" en el encabezado Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="f2d54-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="f2d54-121">Obtención de una cookie</span><span class="sxs-lookup"><span data-stu-id="f2d54-121">Getting a Cookie</span></span>

<span data-ttu-id="f2d54-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) devuelve las cookies para la dirección URL especificada y todas sus direcciones URL primarias.</span><span class="sxs-lookup"><span data-stu-id="f2d54-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="f2d54-123">En el ejemplo siguiente se muestra una llamada a [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span><span class="sxs-lookup"><span data-stu-id="f2d54-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a><span data-ttu-id="f2d54-124">Establecer una cookie</span><span class="sxs-lookup"><span data-stu-id="f2d54-124">Setting a Cookie</span></span>

<span data-ttu-id="f2d54-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) se usa para establecer una cookie en la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="f2d54-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="f2d54-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) puede crear cookies persistentes y de sesión.</span><span class="sxs-lookup"><span data-stu-id="f2d54-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="f2d54-127">Las cookies persistentes tienen una fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="f2d54-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="f2d54-128">Estas cookies se almacenan en la cuenta de usuarios locales en el directorio de usuarios \\ "nombre de usuario" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies y los usuarios \\ "nombreusuario" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies \\ Low Directory para las aplicaciones que se ejecutan con pocos privilegios.</span><span class="sxs-lookup"><span data-stu-id="f2d54-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="f2d54-129">Las cookies de sesión se almacenan en la memoria y solo se puede acceder a ellas mediante el proceso que las creó.</span><span class="sxs-lookup"><span data-stu-id="f2d54-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="f2d54-130">Los datos de la cookie deben tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2d54-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="f2d54-131">Para la fecha de expiración, el formato debe ser:</span><span class="sxs-lookup"><span data-stu-id="f2d54-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="f2d54-132">DAY es la abreviatura de tres letras para el día de la semana, DD es el día del mes, MMM es la abreviatura de tres letras para el mes, AAAA es el año y HH: MM: SS es la hora del día en hora militar.</span><span class="sxs-lookup"><span data-stu-id="f2d54-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="f2d54-133">En el ejemplo siguiente se muestran dos llamadas a [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span><span class="sxs-lookup"><span data-stu-id="f2d54-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="f2d54-134">La primera llamada crea una cookie de sesión y la segunda crea una cookie persistente.</span><span class="sxs-lookup"><span data-stu-id="f2d54-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> <span data-ttu-id="f2d54-135">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="f2d54-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="f2d54-136">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="f2d54-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f2d54-137">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f2d54-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 