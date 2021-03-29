---
title: modificador/Char
description: El modificador/char ayuda a asegurarse de que el compilador de MIDL y el compilador de C funcionan juntos correctamente para todos los tipos Char y Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char modificador MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784240"
---
# <a name="char-switch"></a><span data-ttu-id="2cce7-104">modificador/Char</span><span class="sxs-lookup"><span data-stu-id="2cce7-104">/char switch</span></span>

<span data-ttu-id="2cce7-105">El modificador **/Char** ayuda a asegurarse de que el compilador de MIDL y el compilador de C funcionan juntos correctamente para todos los tipos [**Char**](char-idl.md) y [**Small**](small.md) .</span><span class="sxs-lookup"><span data-stu-id="2cce7-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="2cce7-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="2cce7-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="2cce7-107"><span id="signed"></span><span id="SIGNED"></span>con signo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2cce7-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2cce7-108">Especifica que el tipo de compilador de C predeterminado para [**Char**](char-idl.md) es signed.</span><span class="sxs-lookup"><span data-stu-id="2cce7-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="2cce7-109">Todas las apariciones de **Char** que no vayan acompañadas de una especificación de signo se generan como carácter sin signo.</span><span class="sxs-lookup"><span data-stu-id="2cce7-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="2cce7-110"><span id="unsigned"></span><span id="UNSIGNED"></span>sin signo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2cce7-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2cce7-111">Especifica que el tipo de compilador de C predeterminado para [**Char**](char-idl.md) es sin signo.</span><span class="sxs-lookup"><span data-stu-id="2cce7-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="2cce7-112">Todos los usos de [**pequeño**](small.md) no acompañado por una especificación de signo se generan como pequeños firmados.</span><span class="sxs-lookup"><span data-stu-id="2cce7-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="2cce7-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2cce7-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2cce7-114">Especifica que todos los valores [**Char**](char-idl.md) se van a pasar a los archivos generados sin una palabra clave de signo específica.</span><span class="sxs-lookup"><span data-stu-id="2cce7-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="2cce7-115">Todos los usos de [**pequeño**](small.md) no acompañado por una especificación de signo se generan como **pequeños**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cce7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cce7-116">Remarks</span></span>

<span data-ttu-id="2cce7-117">Por definición, el [**carácter**](char-idl.md) de MIDL es sin signo.</span><span class="sxs-lookup"><span data-stu-id="2cce7-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="2cce7-118">"Small" se define en términos de **Char** ( \# definir caracteres pequeños) y MIDL [**Small**](small.md) está firmado.</span><span class="sxs-lookup"><span data-stu-id="2cce7-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="2cce7-119">El modificador **/Char** indica al compilador de MIDL que especifique declaraciones con [**signo**](signed.md) o [**sin signo**](unsigned.md) explícitas en los archivos generados cuando la declaración de firma del compilador de C entra en conflicto con el valor predeterminado de MIDL para ese tipo.</span><span class="sxs-lookup"><span data-stu-id="2cce7-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="2cce7-120">Recuerde que el compilador MIDL genera el código auxiliar como código fuente de C, que debe compilar como parte de los programas de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="2cce7-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="2cce7-121">Algunos compiladores usan los datos de [**caracteres**](char-idl.md) **Char Everywhere con signo** que se especifican en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="2cce7-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="2cce7-122">El código fuente de código auxiliar que genera el compilador MIDL trata todos los datos **Char** como **Char sin signo**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="2cce7-123">Si el compilador MIDL simplemente generó todos los datos **Char** en el archivo IDL como datos **Char** en el código auxiliar, los compiladores que usan un **carácter signed char** para los datos **Char** causarían un conflicto en el código fuente de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="2cce7-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="2cce7-124">El propósito del modificador de la línea de comandos **/Char** es resolver estos posibles conflictos.</span><span class="sxs-lookup"><span data-stu-id="2cce7-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="2cce7-125">Conserva todos los datos especificados como [**Char**](char-idl.md) en el archivo IDL como **unsigned char** en el código fuente del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="2cce7-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="2cce7-126">También mantiene los datos [**pequeños**](small.md) como firmados.</span><span class="sxs-lookup"><span data-stu-id="2cce7-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="2cce7-127">En la tabla siguiente se resumen los tipos generados.</span><span class="sxs-lookup"><span data-stu-id="2cce7-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="2cce7-128">MIDL/Char, opción</span><span class="sxs-lookup"><span data-stu-id="2cce7-128">midl /char option</span></span>       | <span data-ttu-id="2cce7-129">Tipo char generado</span><span class="sxs-lookup"><span data-stu-id="2cce7-129">Generated char type</span></span> | <span data-ttu-id="2cce7-130">Tipo pequeño generado</span><span class="sxs-lookup"><span data-stu-id="2cce7-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="2cce7-131">**/char de MIDL con signo**</span><span class="sxs-lookup"><span data-stu-id="2cce7-131">**midl /char signed**</span></span>   | <span data-ttu-id="2cce7-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="2cce7-132">**unsigned char**</span></span>   | <span data-ttu-id="2cce7-133">**small**</span><span class="sxs-lookup"><span data-stu-id="2cce7-133">**small**</span></span>            |
| <span data-ttu-id="2cce7-134">**/char de MIDL sin signo**</span><span class="sxs-lookup"><span data-stu-id="2cce7-134">**midl /char unsigned**</span></span> | <span data-ttu-id="2cce7-135">**char**</span><span class="sxs-lookup"><span data-stu-id="2cce7-135">**char**</span></span>            | <span data-ttu-id="2cce7-136">**con signo pequeño**</span><span class="sxs-lookup"><span data-stu-id="2cce7-136">**signed small**</span></span>     |
| <span data-ttu-id="2cce7-137">**ascii7/char MIDL**</span><span class="sxs-lookup"><span data-stu-id="2cce7-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="2cce7-138">**char**</span><span class="sxs-lookup"><span data-stu-id="2cce7-138">**char**</span></span>            | <span data-ttu-id="2cce7-139">**small**</span><span class="sxs-lookup"><span data-stu-id="2cce7-139">**small**</span></span>            |



 

<span data-ttu-id="2cce7-140">La opción **/Char** signed indica que los tipos Char y Small del compilador de C están firmados.</span><span class="sxs-lookup"><span data-stu-id="2cce7-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="2cce7-141">Para que coincida con el valor predeterminado de MIDL para **Char**, el compilador MIDL debe convertir todos los usos de **Char** no acompañados de una especificación de signo a **Char sin signo**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="2cce7-142">No se modifica el tipo [**pequeño**](small.md) porque este valor predeterminado del compilador de C coincide con el valor predeterminado de MIDL para un **pequeño**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="2cce7-143">La opción unsigned de **/Char** indica que el tipo [**Char**](char-idl.md) del compilador de C no tiene signo.</span><span class="sxs-lookup"><span data-stu-id="2cce7-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="2cce7-144">El compilador MIDL convierte todos los usos de [**pequeños**](small.md) no acompañados de una especificación de signo a una **pequeña** **firmada** .</span><span class="sxs-lookup"><span data-stu-id="2cce7-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="2cce7-145">La opción ascii7 indica que no se ha agregado ninguna especificación de signo explícita a los tipos [**Char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="2cce7-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="2cce7-146">El tipo [**Small**](small.md) se genera como **pequeño**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="2cce7-147">Para evitar confusiones, debe utilizar especificaciones de signo explícitas para los tipos [**Char**](char-idl.md) y Small siempre que sea posible en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2cce7-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="2cce7-148">Tenga en cuenta que el uso de tipos **Char** con firma explícita en el archivo IDL no es compatible con DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="2cce7-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="2cce7-149">Por lo tanto, esta característica no está disponible al compilar con el modificador [**/OSF**](-osf.md) de MIDL.</span><span class="sxs-lookup"><span data-stu-id="2cce7-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="2cce7-150">Para obtener más información relacionada con **/Char**, vea [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="2cce7-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2cce7-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2cce7-151">Examples</span></span>

<span data-ttu-id="2cce7-152">**MIDL/char signed nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="2cce7-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="2cce7-153">**/char de MIDL sin signo nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="2cce7-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="2cce7-154">**MIDL/char ascii7 nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="2cce7-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2cce7-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cce7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cce7-156">**char**</span><span class="sxs-lookup"><span data-stu-id="2cce7-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="2cce7-157">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="2cce7-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="2cce7-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2cce7-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="2cce7-159">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="2cce7-159">**small**</span></span>](small.md)
</dt> </dl>

 

 




