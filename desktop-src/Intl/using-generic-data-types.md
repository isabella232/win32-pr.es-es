---
description: Si usa tipos de datos genéricos en el código, se puede compilar para Unicode simplemente mediante una directiva de preprocesador para definir &\# 0034; Unicode&\# 0034; antes de las \# instrucciones include para los archivos de encabezado.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usar tipos de datos genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688699"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="730ae-103">Usar tipos de datos genéricos</span><span class="sxs-lookup"><span data-stu-id="730ae-103">Using Generic Data Types</span></span>

<span data-ttu-id="730ae-104">Si usa tipos de datos genéricos en el código, se puede compilar para [Unicode](unicode.md) simplemente mediante una directiva de preprocesador para definir "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="730ae-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="730ae-105">Para compilar las páginas de códigos de código para [Windows (ANSI)](code-pages.md), omita la definición de "Unicode".</span><span class="sxs-lookup"><span data-stu-id="730ae-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="730ae-106">Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las páginas de códigos variadas y simplificar la localización.</span><span class="sxs-lookup"><span data-stu-id="730ae-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="730ae-107">Para crear código fuente que se puede compilar para utilizar caracteres Unicode y cadenas, o para usar caracteres y cadenas de páginas de códigos de Windows:</span><span class="sxs-lookup"><span data-stu-id="730ae-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="730ae-108">Utilice tipos de datos genéricos, como TCHAR, LPTSTR y LPTCH, para todos los tipos de caracteres y cadenas que se usan para el texto.</span><span class="sxs-lookup"><span data-stu-id="730ae-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="730ae-109">Para obtener más información sobre los tipos genéricos, vea [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="730ae-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="730ae-110">Asegúrese de que los punteros a los búferes de datos que no son de texto o a las matrices de bytes binarias están codificados con tipos de datos como LPBYTE o LPWORD, en lugar del tipo LPTSTR o LPTCH.</span><span class="sxs-lookup"><span data-stu-id="730ae-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="730ae-111">Declare explícitamente punteros de tipo indeterminado como punteros void mediante LPVOID, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="730ae-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="730ae-112">Hacer independiente del tipo aritmético del puntero.</span><span class="sxs-lookup"><span data-stu-id="730ae-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="730ae-113">El uso de unidades de tamaño TCHAR produce variables de 2 bytes si se define Unicode y 1 byte si no se ha definido Unicode.</span><span class="sxs-lookup"><span data-stu-id="730ae-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="730ae-114">El uso de la aritmética de puntero siempre devuelve el número de elementos indicado por el puntero, tanto si los elementos tienen un tamaño de 1 o 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="730ae-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="730ae-115">La siguiente expresión siempre recupera el número de elementos, independientemente de si se ha definido Unicode.</span><span class="sxs-lookup"><span data-stu-id="730ae-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="730ae-116">La siguiente expresión determina el número de bytes utilizados.</span><span class="sxs-lookup"><span data-stu-id="730ae-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="730ae-117">No es necesario cambiar una instrucción como la siguiente, porque el incremento del puntero apunta al siguiente elemento de carácter.</span><span class="sxs-lookup"><span data-stu-id="730ae-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="730ae-118">Reemplazar cadenas literales y constantes de caracteres de manifiesto con macros.</span><span class="sxs-lookup"><span data-stu-id="730ae-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="730ae-119">Cambie las expresiones como las siguientes.</span><span class="sxs-lookup"><span data-stu-id="730ae-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="730ae-120">Use la macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) como se indica a continuación en esta expresión.</span><span class="sxs-lookup"><span data-stu-id="730ae-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="730ae-121">La macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) hace que las cadenas se evalúen como L "cadena" cuando se define Unicode, y como "cadena" en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="730ae-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="730ae-122">Para facilitar la administración, mueva las cadenas literales a los recursos, especialmente si contienen caracteres que están fuera del intervalo ASCII (de 0x00 a 0x7F) o se exponen en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="730ae-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="730ae-123">Para admitir la localización de la aplicación para distintos idiomas nacionales, es muy importante que todas las cadenas de la interfaz de usuario estén en recursos localizables.</span><span class="sxs-lookup"><span data-stu-id="730ae-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="730ae-124">Use las versiones genéricas de las funciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="730ae-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="730ae-125">Para obtener más información, vea [convenciones de los prototipos de función](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="730ae-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="730ae-126">Use las versiones genéricas de las funciones de cadena de la biblioteca estándar de C y recuerde definir " \_ Unicode", así como "Unicode", como se describe en [funciones estándar de C](standard-c-functions.md).</span><span class="sxs-lookup"><span data-stu-id="730ae-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="730ae-127">Si va a adaptar una aplicación escrita originalmente para páginas de códigos de Windows, Recuerde cambiar cualquier código que se base en 255 como el valor más grande de un carácter.</span><span class="sxs-lookup"><span data-stu-id="730ae-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="730ae-128">Al compilar el código que ha escrito tal y como se ha descrito anteriormente, el compilador puede crear versiones de páginas de códigos de Windows y Unicode de la aplicación desde el mismo origen.</span><span class="sxs-lookup"><span data-stu-id="730ae-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="730ae-129">En función de las definiciones de Unicode, las funciones genéricas se resuelven para generar los mismos archivos binarios que si se escribiera código exclusivamente para Unicode o exclusivamente para páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="730ae-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="730ae-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="730ae-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730ae-131">Usar Unicode y juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="730ae-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



