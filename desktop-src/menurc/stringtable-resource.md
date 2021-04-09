---
title: Recurso STRINGTABLE
description: Define uno o más recursos de cadena para una aplicación. Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en null que se pueden cargar cuando es necesario desde el archivo ejecutable, mediante la función LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menús de recursos de STRINGTABLE y otros recursos
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149267"
---
# <a name="stringtable-resource"></a><span data-ttu-id="85553-105">Recurso STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="85553-105">STRINGTABLE resource</span></span>

<span data-ttu-id="85553-106">Define uno o más recursos de cadena para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="85553-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="85553-107">Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en null que se pueden cargar cuando es necesario desde el archivo ejecutable, mediante la función [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .</span><span class="sxs-lookup"><span data-stu-id="85553-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="85553-108">Hay dos maneras de dar formato a una instrucción **stringtable** :</span><span class="sxs-lookup"><span data-stu-id="85553-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="85553-109">\- o -</span><span class="sxs-lookup"><span data-stu-id="85553-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="85553-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85553-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85553-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="85553-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="85553-112">Este parámetro puede ser cero o más de las instrucciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="85553-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="85553-113">.</span><span class="sxs-lookup"><span data-stu-id="85553-113">Statement</span></span>                                                        | <span data-ttu-id="85553-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="85553-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85553-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="85553-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="85553-116">Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="85553-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="85553-117">Para obtener más información, vea [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="85553-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="85553-118">[](language-statement.md) *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="85553-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="85553-119">Especifica el idioma del recurso.</span><span class="sxs-lookup"><span data-stu-id="85553-119">Specifies the language for the resource.</span></span> <span data-ttu-id="85553-120">Para obtener más información, vea [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="85553-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="85553-121">[**Versión**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="85553-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="85553-122">Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="85553-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="85553-123">Para obtener más información, vea [**versión**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="85553-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="85553-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="85553-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="85553-125">Entero de 16 bits sin signo que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="85553-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="85553-126"><span id="string"></span><span id="STRING"></span>*String@*</span><span class="sxs-lookup"><span data-stu-id="85553-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="85553-127">Una o más cadenas, entre comillas.</span><span class="sxs-lookup"><span data-stu-id="85553-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="85553-128">La cadena no debe tener más de 4097 caracteres y debe ocupar una sola línea en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="85553-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="85553-129">Para agregar un retorno de carro a la cadena, use esta secuencia de caracteres: \\ 012.</span><span class="sxs-lookup"><span data-stu-id="85553-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="85553-130">Por ejemplo, "line One \\ 012Line two" define una cadena que se muestra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="85553-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="85553-131">Para insertar comillas en la cadena, use la siguiente secuencia: "".</span><span class="sxs-lookup"><span data-stu-id="85553-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="85553-132">Por ejemplo, "" "línea tres" "" define una cadena que se muestra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="85553-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="85553-133">Para codificar caracteres Unicode, utilice una "L" seguida de los caracteres Unicode entre comillas.</span><span class="sxs-lookup"><span data-stu-id="85553-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="85553-134">Vea la sección ejemplos para obtener un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="85553-134">See the Examples section for an example.</span></span>

<span data-ttu-id="85553-135">El compilador de recursos también admite continuaciones de línea en la *cadena*.</span><span class="sxs-lookup"><span data-stu-id="85553-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="85553-136">Vea la sección ejemplos para obtener un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="85553-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="85553-137">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="85553-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="85553-138">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="85553-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85553-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85553-139">Remarks</span></span>

<span data-ttu-id="85553-140">RC asigna 16 cadenas por sección y usa el valor del identificador para determinar qué sección va a contener la cadena.</span><span class="sxs-lookup"><span data-stu-id="85553-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="85553-141">Las cadenas cuyos identificadores difieren solo en los 4 bits inferiores se colocan en la misma sección.</span><span class="sxs-lookup"><span data-stu-id="85553-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="85553-142">Para obtener más información, vea [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="85553-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="85553-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85553-143">Examples</span></span>

<span data-ttu-id="85553-144">En el ejemplo siguiente se muestra el uso de la instrucción **stringtable** para mostrar cadenas ASCII:</span><span class="sxs-lookup"><span data-stu-id="85553-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="85553-145">En el ejemplo siguiente se muestra cómo codificar caracteres Unicode:</span><span class="sxs-lookup"><span data-stu-id="85553-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="85553-146">En el ejemplo siguiente se muestran cadenas con ASCII y Unicode.</span><span class="sxs-lookup"><span data-stu-id="85553-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="85553-147">Tenga en cuenta que las cadenas sin la "L" inicial usan el formato de escape de 2 dígitos:</span><span class="sxs-lookup"><span data-stu-id="85553-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="85553-148">En el ejemplo siguiente se muestra cómo se pueden usar las continuaciones de línea:</span><span class="sxs-lookup"><span data-stu-id="85553-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="85553-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="85553-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85553-150">**Fall**</span><span class="sxs-lookup"><span data-stu-id="85553-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="85553-151">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="85553-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="85553-152">**SUS**</span><span class="sxs-lookup"><span data-stu-id="85553-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="85553-153">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="85553-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="85553-154">**MENU**</span><span class="sxs-lookup"><span data-stu-id="85553-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="85553-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="85553-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="85553-156">**Versión**</span><span class="sxs-lookup"><span data-stu-id="85553-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 