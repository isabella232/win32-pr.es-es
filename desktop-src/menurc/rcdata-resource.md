---
title: Recurso RCDATA
description: Define un recurso de datos sin procesar para una aplicación. Los recursos de datos sin procesar permiten la inclusión de datos binarios directamente en el archivo ejecutable.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menús de recursos RCDATA y otros recursos
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994762"
---
# <a name="rcdata-resource"></a><span data-ttu-id="fbfeb-105">Recurso RCDATA</span><span class="sxs-lookup"><span data-stu-id="fbfeb-105">RCDATA resource</span></span>

<span data-ttu-id="fbfeb-106">Define un recurso de datos sin procesar para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="fbfeb-107">Los recursos de datos sin procesar permiten la inclusión de datos binarios directamente en el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="fbfeb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbfeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbfeb-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="fbfeb-110">Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="fbfeb-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="fbfeb-112">Este parámetro puede ser cero o más de las instrucciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="fbfeb-113">.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-113">Statement</span></span>                                                        | <span data-ttu-id="fbfeb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbfeb-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbfeb-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="fbfeb-116">Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="fbfeb-117">Para obtener más información, vea [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fbfeb-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="fbfeb-118">[](language-statement.md) *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="fbfeb-119">Idioma del recurso.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-119">Language for the resource.</span></span> <span data-ttu-id="fbfeb-120">Para obtener más información, vea [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fbfeb-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="fbfeb-121">[**Versión**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="fbfeb-122">Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="fbfeb-123">Para obtener más información, vea [**versión**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fbfeb-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="fbfeb-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*datos sin procesar*</span><span class="sxs-lookup"><span data-stu-id="fbfeb-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="fbfeb-125">Datos sin procesar que se componen de uno o varios enteros o cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="fbfeb-126">Los enteros se pueden especificar en formato decimal, octal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="fbfeb-127">Para ser compatible con Windows de 16 bits, los enteros se almacenan como valores de **Word** .</span><span class="sxs-lookup"><span data-stu-id="fbfeb-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="fbfeb-128">Puede almacenar un entero como valor **DWORD** si califica el entero con el sufijo "L".</span><span class="sxs-lookup"><span data-stu-id="fbfeb-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="fbfeb-129">Las cadenas se incluyen entre comillas.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="fbfeb-130">RC no anexa automáticamente un carácter nulo de terminación a una cadena.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="fbfeb-131">Cada cadena es una secuencia de los caracteres ANSI especificados, a menos que la califique como una cadena de caracteres anchos con el prefijo L.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="fbfeb-132">El bloque de datos comienza en un límite **DWORD** y RC no realiza ningún relleno ni alineación de los datos en el bloque de *datos sin procesar* .</span><span class="sxs-lookup"><span data-stu-id="fbfeb-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="fbfeb-133">Es su responsabilidad garantizar la correcta alineación de los datos dentro del bloque.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="fbfeb-134">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="fbfeb-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="fbfeb-135">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="fbfeb-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fbfeb-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fbfeb-136">Examples</span></span>

<span data-ttu-id="fbfeb-137">En el siguiente ejemplo se muestra el uso de la instrucción **RCDATA** :</span><span class="sxs-lookup"><span data-stu-id="fbfeb-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="fbfeb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbfeb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfeb-139">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="fbfeb-140">**SUS**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="fbfeb-141">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="fbfeb-142">**MENU**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="fbfeb-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="fbfeb-144">**Versión**</span><span class="sxs-lookup"><span data-stu-id="fbfeb-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 




