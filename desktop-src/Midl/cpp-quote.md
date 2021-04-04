---
title: cpp_quote (atributo)
description: La \_ palabra clave CPP quote indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote el atributo MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076870"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="a126b-104">\_atributo de Comillas CPP</span><span class="sxs-lookup"><span data-stu-id="a126b-104">cpp\_quote attribute</span></span>

<span data-ttu-id="a126b-105">La palabra clave **CPP \_ Quote** indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="a126b-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="a126b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a126b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a126b-107">*string*</span><span class="sxs-lookup"><span data-stu-id="a126b-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="a126b-108">Especifica una cadena entrecomillada que se emite en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="a126b-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="a126b-109">La cadena debe ir entre comillas para evitar la expansión por parte del preprocesador de C.</span><span class="sxs-lookup"><span data-stu-id="a126b-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a126b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a126b-110">Remarks</span></span>

<span data-ttu-id="a126b-111">El preprocesador del compilador de C procesa las directivas de preprocesamiento de lenguaje c que aparecen en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a126b-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="a126b-112">Las directivas de **\# definición** en el archivo IDL están disponibles durante la compilación de MIDL pero no están disponibles para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="a126b-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="a126b-113">Por ejemplo, cuando el preprocesador encuentra la Directiva " \# definir Windows 4", el preprocesador reemplaza todas las apariciones de "Windows" en el archivo IDL por "4".</span><span class="sxs-lookup"><span data-stu-id="a126b-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="a126b-114">El símbolo "WINDOWS" no está disponible durante la compilación en el lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="a126b-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="a126b-115">Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador de MIDL al compilador de C, use la directiva **\# pragma MIDL \_ echo** o **CPP \_ Quote** .</span><span class="sxs-lookup"><span data-stu-id="a126b-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="a126b-116">Estas directivas indican al compilador de MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas.</span><span class="sxs-lookup"><span data-stu-id="a126b-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="a126b-117">Las directivas **\# pragma MIDL \_ echo** y **CPP \_ Quote** son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a126b-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="a126b-118">El compilador MIDL coloca las cadenas especificadas en las directivas **CPP \_ Quote** y [**pragma**](pragma.md) en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y con respecto a otros componentes de la interfaz en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a126b-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="a126b-119">Las cadenas deben aparecer normalmente en la sección cuerpo de la interfaz de archivo IDL después de todas las operaciones de [**importación**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="a126b-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="a126b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a126b-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="a126b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a126b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a126b-122">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="a126b-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a126b-123">**importar**</span><span class="sxs-lookup"><span data-stu-id="a126b-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="a126b-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="a126b-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




