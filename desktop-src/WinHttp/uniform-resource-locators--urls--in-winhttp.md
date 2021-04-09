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
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="169ae-103">Localizadores de recursos uniformes (URL) en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="169ae-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="169ae-104">Una dirección URL es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet.</span><span class="sxs-lookup"><span data-stu-id="169ae-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="169ae-105">Cada dirección URL está compuesta de un esquema (HTTP, HTTPS, FTP o Gopher) y una cadena específica del esquema.</span><span class="sxs-lookup"><span data-stu-id="169ae-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="169ae-106">Esta cadena también puede incluir una combinación de una ruta de acceso de directorio, una cadena de búsqueda o un nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="169ae-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="169ae-107">Las funciones de los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan la capacidad de crear, combinar, desglosar y canonizar las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="169ae-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="169ae-108">Para obtener más información, vea [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [localizadores de recursos uniformes](https://www.ietf.org/rfc/rfc1738.txt) y [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [identificadores uniformes de recursos (URI): Sintaxis genérica](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="169ae-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="169ae-109">¿Qué es una dirección URL con formato canónico?</span><span class="sxs-lookup"><span data-stu-id="169ae-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="169ae-110">La sintaxis y la semántica especificadas de las direcciones URL dejan espacio para la variación y el error.</span><span class="sxs-lookup"><span data-stu-id="169ae-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="169ae-111">La canonización es el proceso de normalizar una dirección URL real en un formato "canónico", estándar y correcto.</span><span class="sxs-lookup"><span data-stu-id="169ae-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="169ae-112">Esto implica codificar algunos caracteres como "secuencias de escape".</span><span class="sxs-lookup"><span data-stu-id="169ae-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="169ae-113">No es necesario codificar caracteres alfanuméricos de US-ASCII (los dígitos 0-9, las letras mayúsculas A-Z y las letras minúsculas a-z).</span><span class="sxs-lookup"><span data-stu-id="169ae-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="169ae-114">La mayoría de los demás caracteres deben ser caracteres de escape, incluidos los caracteres de control, el carácter de espacio, el signo de porcentaje, los caracteres no seguros (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] y ') y todos los caracteres con un punto de código superior a 127.</span><span class="sxs-lookup"><span data-stu-id="169ae-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="169ae-115">Usar las funciones de WinHTTP para controlar las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="169ae-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="169ae-116">WinHTTP proporciona dos funciones para controlar las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="169ae-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="169ae-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa una dirección URL en sus partes componentes y [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crea una dirección URL a partir de los componentes.</span><span class="sxs-lookup"><span data-stu-id="169ae-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="169ae-118">Separación de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="169ae-118">Separating URLs</span></span>

<span data-ttu-id="169ae-119">La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa una dirección URL en sus partes componentes y devuelve los componentes indicados por la estructura de [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="169ae-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="169ae-120">Los componentes que componen la estructura de los [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) son el número de esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso URL e información adicional, como los parámetros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="169ae-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="169ae-121">Cada componente, excepto el esquema y los números de puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena.</span><span class="sxs-lookup"><span data-stu-id="169ae-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="169ae-122">El esquema y los números de Puerto solo tienen un miembro que almacena el valor correspondiente. se devuelven el esquema y los números de puerto en todas las llamadas correctas a [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span><span class="sxs-lookup"><span data-stu-id="169ae-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="169ae-123">Para recuperar el valor de un componente determinado en la estructura de [**\_ los componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , el miembro que almacena la longitud de cadena de ese componente debe establecerse en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="169ae-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="169ae-124">El miembro de cadena puede ser un puntero a un búfer o **null**.</span><span class="sxs-lookup"><span data-stu-id="169ae-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="169ae-125">Si el miembro de puntero contiene un puntero a un búfer, el miembro de longitud de cadena debe contener el tamaño de dicho búfer.</span><span class="sxs-lookup"><span data-stu-id="169ae-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="169ae-126">La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) devuelve la información del componente como una cadena en el búfer y almacena la longitud de la cadena en el miembro de longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="169ae-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="169ae-127">Si el miembro de puntero se establece en **null**, el miembro de longitud de cadena se puede establecer en cualquier valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="169ae-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="169ae-128">La función [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) almacena un puntero al primer carácter de la cadena de dirección URL que contiene la información del componente y establece la longitud de la cadena en el número de caracteres de la parte restante de la cadena de dirección URL que pertenece al componente.</span><span class="sxs-lookup"><span data-stu-id="169ae-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="169ae-129">Todos los miembros de puntero se establecen en **null** con un punto de miembro de longitud distinto de cero en el punto de inicio adecuado en la cadena de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="169ae-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="169ae-130">La longitud almacenada en el miembro de longitud debe usarse para determinar el final de la información del componente individual.</span><span class="sxs-lookup"><span data-stu-id="169ae-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="169ae-131">Para finalizar la inicialización correcta de la estructura de los [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , el miembro **dwStructSize** debe establecerse en el tamaño de la estructura de los [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .</span><span class="sxs-lookup"><span data-stu-id="169ae-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="169ae-132">Creación de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="169ae-132">Creating URLs</span></span>

<span data-ttu-id="169ae-133">La función [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa la información de la estructura de [**\_ componentes URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descritos anteriormente para crear una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="169ae-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="169ae-134">Para cada componente necesario, el miembro de puntero debe contener un puntero al búfer que contiene la información.</span><span class="sxs-lookup"><span data-stu-id="169ae-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="169ae-135">El miembro de longitud debe establecerse en cero si el miembro de puntero contiene un puntero a una cadena terminada en cero; el miembro de longitud debe establecerse en la longitud de la cadena si el miembro del puntero contiene un puntero a una cadena que no termina en cero.</span><span class="sxs-lookup"><span data-stu-id="169ae-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="169ae-136">El miembro de puntero de cualquier componente que no sea necesario debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="169ae-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="169ae-137">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="169ae-137">Sample code</span></span>

<span data-ttu-id="169ae-138">En el código de ejemplo siguiente se muestra cómo usar [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) y [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) para desensamblar una dirección URL existente, modificar uno de sus componentes y volver a ensamblarlo en una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="169ae-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


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



 

 



