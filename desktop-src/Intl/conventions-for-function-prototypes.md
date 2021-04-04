---
description: El Windows SDK proporciona prototipos de función en las versiones genérica, de la página de códigos de Windows y Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenciones para Prototipos de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910122"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="54adc-103">Convenciones para Prototipos de función</span><span class="sxs-lookup"><span data-stu-id="54adc-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="54adc-104">El Windows SDK proporciona prototipos de función en las versiones genérica, de la [Página de códigos de Windows](code-pages.md)y [Unicode](unicode.md) .</span><span class="sxs-lookup"><span data-stu-id="54adc-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="54adc-105">Los prototipos se pueden compilar para generar prototipos de páginas de códigos de Windows o prototipos Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="54adc-106">Los tres prototipos se describen en este tema y se muestran en los ejemplos de código para la función [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="54adc-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="54adc-107">A continuación se muestra un ejemplo de un prototipo genérico:</span><span class="sxs-lookup"><span data-stu-id="54adc-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="54adc-108">El archivo de encabezado proporciona el nombre de función genérico implementado como una macro.</span><span class="sxs-lookup"><span data-stu-id="54adc-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="54adc-109">El preprocesador expande la macro en la página de códigos de Windows o en el nombre de la función Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="54adc-110">La letra "A" (ANSI) o "W" (Unicode) se agrega al final del nombre de la función genérica, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="54adc-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="54adc-111">A continuación, el archivo de encabezado proporciona dos prototipos específicos, uno para las páginas de códigos de Windows y otro para Unicode, tal y como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="54adc-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="54adc-112">Como se explica en [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md), el prototipo de función genérica usa el tipo de datos LPCTSTR para el parámetro text.</span><span class="sxs-lookup"><span data-stu-id="54adc-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="54adc-113">Sin embargo, el prototipo de la página de códigos de Windows utiliza el tipo LPCSTR, y el prototipo Unicode utiliza LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="54adc-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="54adc-114">Para todas las características con argumentos de texto, las aplicaciones deben utilizar normalmente los prototipos genéricos de la función.</span><span class="sxs-lookup"><span data-stu-id="54adc-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="54adc-115">Si una aplicación define "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación, las instrucciones se compilarán en funciones Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="54adc-116">Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las distintas páginas de códigos y para facilitar la localización.</span><span class="sxs-lookup"><span data-stu-id="54adc-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="54adc-117">Deben escribirse con funciones genéricas y deben definir Unicode para compilar las funciones en funciones Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="54adc-118">En los pocos lugares donde una aplicación debe trabajar con datos de caracteres de 8 bits, puede hacer el uso explícito de las funciones para las páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="54adc-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="54adc-119">La aplicación debe utilizar siempre un prototipo genérico de la función con cadena y tipos de caracteres genéricos.</span><span class="sxs-lookup"><span data-stu-id="54adc-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="54adc-120">Todos los nombres de funciones que terminen con una “W” mayúscula utilizan Unicode, es decir, carácter, parámetros anchos.</span><span class="sxs-lookup"><span data-stu-id="54adc-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="54adc-121">Algunas funciones solo existen en las versiones Unicode y solo se pueden usar con los tipos de datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="54adc-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="54adc-122">Por ejemplo, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) y [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) solo tienen versiones Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="54adc-123">La sección de requisitos de la documentación de referencia de cada función de Unicode y de juego de caracteres proporciona información sobre las versiones de funciones implementadas por los sistemas operativos compatibles.</span><span class="sxs-lookup"><span data-stu-id="54adc-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="54adc-124">Si se incluye una línea que empieza por "Unicode", la función tiene versiones independientes de la página de códigos de Windows y Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="54adc-125">Cuando una función tiene un parámetro de longitud para una cadena de caracteres, la longitud debe documentarse como un recuento de los valores TCHAR de la cadena.</span><span class="sxs-lookup"><span data-stu-id="54adc-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="54adc-126">Este tipo de datos hace referencia a los bytes de las versiones de la página de códigos de Windows de la función o de las palabras de 16 bits para las versiones Unicode.</span><span class="sxs-lookup"><span data-stu-id="54adc-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="54adc-127">Sin embargo, las funciones que requieren o devuelven punteros a bloques de memoria sin tipo, como la función [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , generalmente toman un tamaño en bytes, independientemente del prototipo que se use.</span><span class="sxs-lookup"><span data-stu-id="54adc-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="54adc-128">Si la asignación de memoria sin tipo es para una cadena, la aplicación debe multiplicar el número de caracteres por sizeof (TCHAR).</span><span class="sxs-lookup"><span data-stu-id="54adc-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="54adc-129">Para obtener más información, vea [usar tipos de datos genéricos](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="54adc-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54adc-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54adc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54adc-131">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="54adc-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
