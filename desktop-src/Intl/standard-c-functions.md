---
description: Las bibliotecas en tiempo de ejecución estándar de C contienen versiones Unicode UTF-16 (caracteres anchos) de funciones de cadena que se pueden usar con versiones Unicode y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de juegos de caracteres de un solo byte (SBCSs). El tipo de datos Unicode WCHAR es compatible con el tipo de datos WCHAR \_ t en ANSI C y permite el acceso a las funciones de cadena Unicode. Las versiones Unicode de las funciones comienzan con las letras &\# 0034; wcs&\# 0034; (o a veces &\# 0034; \_ WCS&\# 0034;). El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres. Las versiones de caracteres de las funciones comienzan con las letras &\# 0034; str&\# 0034;. También hay versiones especiales de juegos de caracteres de doble byte (DBCS) que comienzan con las letras &\# 0034; \_ MBS&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funciones estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913522"
---
# <a name="standard-c-functions"></a><span data-ttu-id="54165-108">Funciones estándar de C</span><span class="sxs-lookup"><span data-stu-id="54165-108">Standard C Functions</span></span>

<span data-ttu-id="54165-109">Las bibliotecas en tiempo de ejecución estándar de C contienen versiones Unicode UTF-16 (caracteres anchos) de funciones de cadena que se pueden usar con versiones [Unicode](unicode.md) y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de [juegos de caracteres de un solo byte](single-byte-character-sets.md) (SBCSs).</span><span class="sxs-lookup"><span data-stu-id="54165-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="54165-110">El tipo de datos Unicode WCHAR es compatible con el tipo de datos WCHAR \_ t en ANSI C y permite el acceso a las funciones de cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="54165-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="54165-111">Las versiones Unicode de las funciones comienzan con las letras "WCS" (o a veces " \_ WCS").</span><span class="sxs-lookup"><span data-stu-id="54165-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="54165-112">El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54165-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="54165-113">Las versiones de caracteres de las funciones comienzan con las letras "STR".</span><span class="sxs-lookup"><span data-stu-id="54165-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="54165-114">También hay versiones especiales de [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) que comienzan con las letras " \_ MBS".</span><span class="sxs-lookup"><span data-stu-id="54165-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="54165-115">Las bibliotecas en tiempo de ejecución estándar de C incluyen funciones genéricas para todas las funciones de cadena estándar de C.</span><span class="sxs-lookup"><span data-stu-id="54165-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="54165-116">Comienzan con " \_ TCS" y se enumeran en el archivo de encabezado TCHAR. h.</span><span class="sxs-lookup"><span data-stu-id="54165-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="54165-117">Estas funciones usan el tipo de datos TCHAR genérico.</span><span class="sxs-lookup"><span data-stu-id="54165-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="54165-118">Una aplicación debe agregar las siguientes líneas para usar las funciones genéricas y compilar para Unicode.</span><span class="sxs-lookup"><span data-stu-id="54165-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="54165-119">Tenga en cuenta que los archivos TCHAR. h y WCHAR. h son obligatorios y que también se requiere el carácter de subrayado inicial en la \_ variable Unicode.</span><span class="sxs-lookup"><span data-stu-id="54165-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="54165-120">Esta nomenclatura es específica de la biblioteca estándar de C.</span><span class="sxs-lookup"><span data-stu-id="54165-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="54165-121">"Unicode" se representa sin el carácter de subrayado para Microsoft Windows en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="54165-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="54165-122">Las funciones [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) y [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) pueden convertir desde el juego de caracteres compatible con la biblioteca estándar de C a Unicode y viceversa, con algunas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="54165-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="54165-123">Para obtener más información sobre la traducción de cadenas a y desde Unicode, vea [traducción entre tipos de cadena](translation-between-string-types.md).</span><span class="sxs-lookup"><span data-stu-id="54165-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="54165-124">La función [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definida en TCHAR. h admite las mismas especificaciones de formato que las funciones de impresión strsafe. h, por ejemplo [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span><span class="sxs-lookup"><span data-stu-id="54165-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="54165-125">Del mismo modo, TCHAR. h define una función [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , en la que la propia cadena de formato es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="54165-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="54165-126">Un control deficiente del búfer es implicado en muchos problemas de seguridad que implican saturaciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="54165-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="54165-127">Consulte [referencia de strsafe. h](../menurc/strsafe-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="54165-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="54165-128">Las funciones definidas en strsafe. h proporcionan procesamiento adicional para el control de búfer adecuado en el código.</span><span class="sxs-lookup"><span data-stu-id="54165-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="54165-129">Están diseñados para reemplazar sus homólogos de C/C++ integrados, así como implementaciones específicas de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="54165-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="54165-130">Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="54165-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54165-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54165-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54165-132">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="54165-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
