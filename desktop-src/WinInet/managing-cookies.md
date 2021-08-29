---
title: Administración de cookies
description: En el protocolo http, un servidor o un script usa cookies para mantener la información de estado en la estación de trabajo cliente.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0931de8b1d9d25862344658bddaacf5fd1d4325f9343176acb0206dcb3e1e383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113625"
---
# <a name="managing-cookies"></a>Administración de cookies

En el protocolo http, un servidor o un script usa cookies para mantener la información de estado en la estación de trabajo cliente. Las funciones de WinINet han implementado una base de datos de cookies persistente para este propósito. Se pueden usar para establecer cookies en y acceder a ellas desde la base de datos de cookies. Para obtener más información, vea [Http Cookies](http-cookies.md).

Las [**funciones InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) [**e InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) se pueden usar para administrar cookies.

## <a name="using-cookie-functions"></a>Uso de funciones de cookies

Las siguientes funciones permiten a una aplicación crear o recuperar cookies en la base de datos de cookies.



| Función                                       | Descripción                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Recupera las cookies para la dirección URL especificada y todas sus direcciones URL primarias. |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Establece una cookie en la dirección URL especificada.                              |



 

Tenga en cuenta que estas funciones no requieren una llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Las cookies que tienen una fecha de expiración se almacenan en la cuenta de usuarios locales en el directorio \\ Usuarios "username" AppData Roaming Microsoft Windows Cookies y en el directorio \\ \\ \\ \\ \\ \\ AppData Roaming Microsoft Windows Cookies \\ \\ \\ \\ \\ \\ Low para aplicaciones que se ejecutan con pocos privilegios. Las cookies que no tienen una fecha de expiración se almacenan en memoria y solo están disponibles para el proceso en el que se crearon.

Como se indicó en el tema Cookies [HTTP,](http-cookies.md) la función [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) no devuelve las cookies marcadas por el servidor como no que admiten scripts con el atributo "HttpOnly" en el encabezado Set-Cookie.

### <a name="getting-a-cookie"></a>Obtención de una cookie

[**InternetGetCookie devuelve**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) las cookies de la dirección URL especificada y todas sus direcciones URL primarias.

En el ejemplo siguiente se muestra una llamada a [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).


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



### <a name="setting-a-cookie"></a>Establecimiento de una cookie

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) se usa para establecer una cookie en la dirección URL especificada. [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) puede crear cookies de sesión y persistentes.

Las cookies persistentes tienen una fecha de expiración. Estas cookies se almacenan en la cuenta de usuarios locales en el directorio Usuarios "nombre de usuario" AppData Roaming Microsoft Windows Cookies y el directorio "nombre de usuario" usuarios \\ \\ \\ \\ \\ \\ \\ AppData Roaming Microsoft Windows Cookies \\ \\ \\ \\ \\ \\ Low para aplicaciones que se ejecutan con pocos privilegios.

Las cookies de sesión se almacenan en memoria y solo el proceso que las creó puede acceder a ellas.

Los datos de la cookie deben tener el formato siguiente:

``` syntax
NAME=VALUE
```

Para la fecha de expiración, el formato debe ser:

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

DAY es la abreviatura de tres letras para el día de la semana, DD es el día del mes, MMM es la abreviatura de tres letras del mes, YYYY es el año y HH:MM:SS es la hora del día en tiempo de las fuerzas.

En el ejemplo siguiente se muestran dos llamadas a [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea). La primera llamada crea una cookie de sesión y la segunda crea una cookie persistente.


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
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 