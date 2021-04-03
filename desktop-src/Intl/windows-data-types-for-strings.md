---
description: La mayoría de las operaciones de cadena pueden utilizar la misma lógica para Unicode y para las páginas de códigos de Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de datos de Windows para cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083476"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="3fe37-103">Tipos de datos de Windows para cadenas</span><span class="sxs-lookup"><span data-stu-id="3fe37-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="3fe37-104">La mayoría de las operaciones de cadena pueden utilizar la misma lógica para [Unicode](unicode.md) y para [las páginas de códigos de Windows](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="3fe37-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="3fe37-105">La única diferencia es que la unidad básica de operación es un carácter de 16 bits (también conocido como carácter ancho) para Unicode y un carácter de 8 bits para las páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fe37-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="3fe37-106">Los archivos de encabezado de Windows proporcionan varias definiciones de tipos que facilitan la creación de orígenes que se pueden compilar para Unicode o para páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fe37-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="3fe37-107">Windows admite tres conjuntos de tipos de datos de caracteres y cadenas: un conjunto de definiciones de tipo genérico que se pueden compilar para páginas de códigos Unicode o Windows, y dos conjuntos de definiciones de tipo específicas.</span><span class="sxs-lookup"><span data-stu-id="3fe37-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="3fe37-108">Un conjunto de definiciones de tipo específico es para su uso con Unicode y el otro es para su uso con las páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fe37-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="3fe37-109">Una aplicación que usa tipos de datos genéricos se puede compilar para Unicode simplemente definiendo "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="3fe37-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="3fe37-110">Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las páginas de códigos variadas y para simplificar la localización.</span><span class="sxs-lookup"><span data-stu-id="3fe37-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="3fe37-111">Deben escribirse con tipos de datos genéricos y deben definir "Unicode" para compilar estos tipos en tipos Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fe37-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="3fe37-112">En los pocos lugares donde una aplicación debe trabajar con datos de caracteres de 8 bits, puede hacer un uso explícito de los tipos de las páginas de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fe37-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="3fe37-113">La capacidad de compilar los tipos genéricos en tipos de páginas de códigos de Windows existe principalmente para la compatibilidad con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="3fe37-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="3fe37-114">Para compilar las páginas de códigos de Windows, la aplicación simplemente omite la definición de Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fe37-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="3fe37-115">En el ejemplo siguiente se muestra el método utilizado en los archivos de encabezado de Windows para definir los tres conjuntos de tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="3fe37-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="3fe37-116">Para la implementación, vea el archivo de encabezado Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="3fe37-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="3fe37-117">La letra "T" de una definición de tipo, por ejemplo, TCHAR o LPTSTR, designa un tipo genérico que se puede compilar para páginas de códigos de Windows o Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fe37-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="3fe37-118">La letra "W" de una definición de tipo, por ejemplo, WCHAR o LPWSTR, designa un tipo Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fe37-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="3fe37-119">Dado que las páginas de códigos de Windows tienen el formato anterior, tienen definiciones de tipos simples, como CHAR y LPSTR.</span><span class="sxs-lookup"><span data-stu-id="3fe37-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="3fe37-120">Para obtener una descripción completa de los tipos de datos de Windows, vea [tipos de datos de Windows](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="3fe37-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe37-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fe37-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe37-122">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="3fe37-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
