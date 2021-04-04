---
title: Diccionario de nombres para mostrar del conjunto de propiedades
description: Un diccionario de nombres para mostrar de propiedades permite que los usuarios del conjunto de propiedades adjunten significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792952"
---
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="b9524-103">Diccionario de nombres para mostrar del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="b9524-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="b9524-104">Un diccionario de nombres para mostrar de propiedades permite que los usuarios del conjunto de propiedades adjunten significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b9524-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="b9524-105">Estructura del Diccionario</span><span class="sxs-lookup"><span data-stu-id="b9524-105">Dictionary Structure</span></span>

<span data-ttu-id="b9524-106">El diccionario contiene un recuento de las entradas de la lista, seguida de una lista de entradas del diccionario.</span><span class="sxs-lookup"><span data-stu-id="b9524-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="b9524-107">Estructura de entrada del Diccionario</span><span class="sxs-lookup"><span data-stu-id="b9524-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="b9524-108">Cada entrada del Diccionario de la lista es un par identificador/cadena de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b9524-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="b9524-109">La siguiente es una definición de pseudo estructura para una entrada de diccionario.</span><span class="sxs-lookup"><span data-stu-id="b9524-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="b9524-110">Es una pseudo estructura porque el \[ \] miembro SZ tiene un tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="b9524-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="b9524-111">Diccionario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9524-111">Sample Dictionary</span></span>

<span data-ttu-id="b9524-112">El siguiente ejemplo de transferencia de datos de mercado de acciones podría incluir un nombre que se puede mostrar "cotización de bolsa" para todo el conjunto y "símbolo del indicador" para el símbolo del PID \_ .</span><span class="sxs-lookup"><span data-stu-id="b9524-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="b9524-113">Si un conjunto de propiedades solo contiene un símbolo y el diccionario, la sección del conjunto de propiedades tendría un flujo de bytes similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9524-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

<span data-ttu-id="b9524-114">Tenga en cuenta los siguientes problemas relacionados con los diccionarios de conjuntos de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b9524-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="b9524-115">El ID. de propiedad 0 no tiene un indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b9524-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="b9524-116">El tipo de datos **DWORD** que indica el recuento de entradas se encuentra en la posición del indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b9524-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="b9524-117">El recuento de caracteres de la cadena *CCH* incluye el carácter cero que termina la cadena.</span><span class="sxs-lookup"><span data-stu-id="b9524-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="b9524-118">Cuando la página de códigos de la propiedad establecida no es Unicode, este campo es realmente un recuento de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="b9524-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="b9524-119">En el caso de los conjuntos de propiedades con una versión de formato de 0, este recuento no puede superar 256.</span><span class="sxs-lookup"><span data-stu-id="b9524-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="b9524-120">En el caso de los conjuntos de propiedades con una versión de formato de 1, este recuento puede ser tan grande como el permitido por el tamaño total del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9524-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="b9524-121">El diccionario es opcional.</span><span class="sxs-lookup"><span data-stu-id="b9524-121">The dictionary is optional.</span></span> <span data-ttu-id="b9524-122">No todos los nombres de las propiedades del conjunto deben aparecer en el diccionario.</span><span class="sxs-lookup"><span data-stu-id="b9524-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="b9524-123">Por el contrario, no es necesario que todos los nombres del diccionario se correspondan con las propiedades del conjunto.</span><span class="sxs-lookup"><span data-stu-id="b9524-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="b9524-124">El Diccionario debe omitir las entradas de las propiedades que se supone que las aplicaciones que manipulan el conjunto de propiedades reconocen universalmente.</span><span class="sxs-lookup"><span data-stu-id="b9524-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="b9524-125">Normalmente, se omiten los nombres de los conjuntos de propiedades base para los estándares ampliamente aceptados, pero los conjuntos de propiedades de uso especial pueden incluir diccionarios para que los usen los exploradores.</span><span class="sxs-lookup"><span data-stu-id="b9524-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="b9524-126">Los nombres de propiedad del diccionario se almacenan en la página de códigos indicada por el [identificador de propiedad 1](/windows/desktop/Stg/reserved-property-identifiers).</span><span class="sxs-lookup"><span data-stu-id="b9524-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="b9524-127">En las páginas de códigos ANSI, cada entrada del diccionario está alineada en bytes.</span><span class="sxs-lookup"><span data-stu-id="b9524-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="b9524-128">Por lo tanto, no hay ningún espacio entre los nombres de propiedad con el identificador de propiedad 0.</span><span class="sxs-lookup"><span data-stu-id="b9524-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="b9524-129">Este es el único caso en el que no es necesario que los valores de los tipos de datos **DWORD** (el identificador de propiedad y la longitud de la propiedad **DWORD** s) estén alineados en los límites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b9524-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="b9524-130">En las páginas Unicode, cada entrada del diccionario tiene una alineación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b9524-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="b9524-131">Los nombres de propiedad que comienzan con los caracteres Unicode binarios 0x0001 a 0x001F se reservan para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b9524-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="b9524-132">El nombre de propiedad asociado a la propiedad ID 0 representa el nombre del conjunto completo de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9524-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 