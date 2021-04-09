---
description: Una dirección URL es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: Localizadores de recursos uniformes (URL) en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082454"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>Localizadores de recursos uniformes (URL) en WinHTTP

Una dirección URL es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet. Cada dirección URL está compuesta de un esquema (HTTP, HTTPS, FTP o Gopher) y una cadena específica del esquema. Esta cadena también puede incluir una combinación de una ruta de acceso de directorio, una cadena de búsqueda o un nombre del recurso. Las funciones de los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan la capacidad de crear, combinar, desglosar y canonizar las direcciones URL. Para obtener más información, vea [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [localizadores de recursos uniformes](https://www.ietf.org/rfc/rfc1738.txt) y [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [identificadores uniformes de recursos (URI): Sintaxis genérica](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>¿Qué es una dirección URL con formato canónico?

La sintaxis y la semántica especificadas de las direcciones URL dejan espacio para la variación y el error. La canonización es el proceso de normalizar una dirección URL real en un formato "canónico", estándar y correcto.

Esto implica codificar algunos caracteres como "secuencias de escape". No es necesario codificar caracteres alfanuméricos de US-ASCII (los dígitos 0-9, las letras mayúsculas A-Z y las letras minúsculas a-z). La mayoría de los demás caracteres deben ser caracteres de escape, incluidos los caracteres de control, el carácter de espacio, el signo de porcentaje, los caracteres no seguros (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] y ') y todos los caracteres con un punto de código superior a 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Usar las funciones de WinHTTP para controlar las direcciones URL

WinHTTP proporciona dos funciones para controlar las direcciones URL. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa una dirección URL en sus partes componentes y [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crea una dirección URL a partir de los componentes.

### <a name="separating-urls"></a>Separación de direcciones URL

La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa una dirección URL en sus partes componentes y devuelve los componentes indicados por la estructura de [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) que se pasa a la función.

Los componentes que componen la estructura de los [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) son el número de esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso URL e información adicional, como los parámetros de búsqueda. Cada componente, excepto el esquema y los números de puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena. El esquema y los números de Puerto solo tienen un miembro que almacena el valor correspondiente. se devuelven el esquema y los números de puerto en todas las llamadas correctas a [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).

Para recuperar el valor de un componente determinado en la estructura de [**\_ los componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , el miembro que almacena la longitud de cadena de ese componente debe establecerse en un valor distinto de cero. El miembro de cadena puede ser un puntero a un búfer o **null**.

Si el miembro de puntero contiene un puntero a un búfer, el miembro de longitud de cadena debe contener el tamaño de dicho búfer. La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) devuelve la información del componente como una cadena en el búfer y almacena la longitud de la cadena en el miembro de longitud de la cadena.

Si el miembro de puntero se establece en **null**, el miembro de longitud de cadena se puede establecer en cualquier valor distinto de cero. La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) almacena un puntero al primer carácter de la cadena de dirección URL que contiene la información del componente y establece la longitud de la cadena en el número de caracteres de la parte restante de la cadena de dirección URL que pertenece al componente.

Todos los miembros de puntero se establecen en **null** con un punto de miembro de longitud distinto de cero en el punto de inicio adecuado en la cadena de dirección URL. La longitud almacenada en el miembro de longitud debe usarse para determinar el final de la información del componente individual.

Para finalizar la inicialización correcta de la estructura de los [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , el miembro **dwStructSize** debe establecerse en el tamaño de la estructura de los [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .

### <a name="creating-urls"></a>Creación de direcciones URL

La función [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa la información de la estructura de [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descritos anteriormente para crear una dirección URL.

Para cada componente necesario, el miembro de puntero debe contener un puntero al búfer que contiene la información. El miembro de longitud debe establecerse en cero si el miembro de puntero contiene un puntero a una cadena terminada en cero; el miembro de longitud debe establecerse en la longitud de la cadena si el miembro del puntero contiene un puntero a una cadena que no termina en cero. El miembro de puntero de cualquier componente que no sea necesario debe establecerse en **null**.

### <a name="sample-code"></a>Código de ejemplo

En el código de ejemplo siguiente se muestra cómo usar [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) y [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) para desensamblar una dirección URL existente, modificar uno de sus componentes y volver a ensamblarlo en una nueva dirección URL.


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



