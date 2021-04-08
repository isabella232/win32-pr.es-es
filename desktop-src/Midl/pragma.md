---
title: pragma (atributo)
description: La Directiva \ pragma MIDL \_ echo indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma (atributo) MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994637"
---
# <a name="pragma-attribute"></a><span data-ttu-id="43441-104">pragma (atributo)</span><span class="sxs-lookup"><span data-stu-id="43441-104">pragma attribute</span></span>

<span data-ttu-id="43441-105">La \# directiva **pragma MIDL \_ echo** indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="43441-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="43441-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43441-107">*string*</span><span class="sxs-lookup"><span data-stu-id="43441-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="43441-108">Especifica una cadena que se inserta en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="43441-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="43441-109">Las comillas se quitan durante el proceso de inserción.</span><span class="sxs-lookup"><span data-stu-id="43441-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="43441-110">*secuencia de tokens*</span><span class="sxs-lookup"><span data-stu-id="43441-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="43441-111">Especifica una secuencia de tokens que se insertan en el archivo de encabezado generado como parte de una directiva **\# pragma** sin ser procesados por el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="43441-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="43441-112">*n*</span><span class="sxs-lookup"><span data-stu-id="43441-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="43441-113">Especifica el tamaño actual del paquete.</span><span class="sxs-lookup"><span data-stu-id="43441-113">Specifies the current pack size.</span></span> <span data-ttu-id="43441-114">Los valores válidos son 1, 2, 4, 8 y 16.</span><span class="sxs-lookup"><span data-stu-id="43441-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="43441-115">*id*</span><span class="sxs-lookup"><span data-stu-id="43441-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="43441-116">Especifica el identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="43441-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43441-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43441-117">Remarks</span></span>

<span data-ttu-id="43441-118">El preprocesador del compilador de C procesa las directivas de preprocesamiento de lenguaje c que aparecen en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="43441-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="43441-119">Las directivas de **\# definición** en el archivo IDL están disponibles durante la compilación de MIDL, aunque no en el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="43441-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="43441-120">Por ejemplo, cuando el preprocesador encuentra la Directiva " \# definir Windows 4", el preprocesador reemplaza todas las apariciones de "Windows" en el archivo IDL por "4".</span><span class="sxs-lookup"><span data-stu-id="43441-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="43441-121">El símbolo "WINDOWS" no está disponible en tiempo de compilación de C.</span><span class="sxs-lookup"><span data-stu-id="43441-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="43441-122">Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador de MIDL al compilador de C, use la directiva **\# pragma MIDL \_ echo** o [**CPP \_ Quote**](cpp-quote.md) .</span><span class="sxs-lookup"><span data-stu-id="43441-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="43441-123">Estas directivas indican al compilador de MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas.</span><span class="sxs-lookup"><span data-stu-id="43441-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="43441-124">Las directivas **\# pragma MIDL \_ echo** y **CPP \_ Quote** son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="43441-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="43441-125">El compilador MIDL utiliza la directiva **\# pragma Pack** para controlar el empaquetado de estructuras.</span><span class="sxs-lookup"><span data-stu-id="43441-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="43441-126">Invalida el modificador de la línea de comandos [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="43441-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="43441-127">La opción Pack (*n*) establece el tamaño actual del paquete en un valor específico: 1, 2, 4, 8 o 16.</span><span class="sxs-lookup"><span data-stu-id="43441-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="43441-128">Las opciones de Pack (de extracción) y de paquete (pop) tienen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="43441-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="43441-129">El compilador mantiene una pila de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="43441-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="43441-130">Los elementos de la pila de empaquetado incluyen un tamaño de paquete y un *identificador* opcional. La pila solo está limitada por la memoria disponible con el tamaño de paquete actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="43441-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="43441-131">Pack (push) hace que el tamaño actual del paquete se inserte en la pila de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="43441-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="43441-132">La pila está limitada por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="43441-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="43441-133">Pack (Inserte,*n*) es el mismo que Pack (Inserte) seguido del Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="43441-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="43441-134">Pack (Inserte, *ID*) también inserciones el *identificador* en la pila de empaquetado junto con el tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="43441-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="43441-135">Pack (inserciones, *ID.*, *n*) es el mismo que el Pack (Inserte, *ID*) seguido de Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="43441-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="43441-136">Pack (pop) da como resultado la extracción de la pila de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="43441-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="43441-137">Los pop desequilibrados causan advertencias y establecen el tamaño actual del paquete en el valor de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="43441-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="43441-138">Si se especifica Pack (pop, *ID*, *n*), se omite *n* .</span><span class="sxs-lookup"><span data-stu-id="43441-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="43441-139">El compilador MIDL coloca las cadenas especificadas en las directivas [**\\ CPP \_ Quote**](cpp-quote.md) y **pragma** en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y con respecto a otros componentes de la interfaz en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="43441-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="43441-140">Las cadenas deben aparecer normalmente en la sección del cuerpo de la interfaz del archivo IDL después de todas las operaciones de [**importación**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="43441-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="43441-141">El compilador MIDL no intenta procesar directivas **\# pragma** que no empiecen por el prefijo "MIDL" \_ .</span><span class="sxs-lookup"><span data-stu-id="43441-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="43441-142">Otras directivas **\# pragma** del archivo IDL se pasan al archivo de encabezado generado sin cambios.</span><span class="sxs-lookup"><span data-stu-id="43441-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="43441-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="43441-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="43441-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="43441-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43441-145">**comilla CPP \_**</span><span class="sxs-lookup"><span data-stu-id="43441-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="43441-146">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="43441-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="43441-147">**importar**</span><span class="sxs-lookup"><span data-stu-id="43441-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="43441-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="43441-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




