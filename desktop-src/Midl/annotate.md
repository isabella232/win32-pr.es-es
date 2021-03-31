---
title: atributo de anotación
description: El atributo \ Anotate \ permite especificar una cadena de anotación SAL para el método, el parámetro o el campo de estructura especificado.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- atributo de anotación MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795214"
---
# <a name="annotate-attribute"></a><span data-ttu-id="f5c61-104">atributo de anotación</span><span class="sxs-lookup"><span data-stu-id="f5c61-104">annotate attribute</span></span>

<span data-ttu-id="f5c61-105">El atributo **\[ Anotate \]** permite especificar una cadena de anotación sal para el método, el parámetro o el campo de estructura especificado.</span><span class="sxs-lookup"><span data-stu-id="f5c61-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="f5c61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5c61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c61-107">*string*</span><span class="sxs-lookup"><span data-stu-id="f5c61-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-108">Cadena de anotación SAL especificada.</span><span class="sxs-lookup"><span data-stu-id="f5c61-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-109">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="f5c61-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-110">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="f5c61-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="f5c61-111">Los atributos de función válidos incluyen la [**\[ devolución \] de llamada**](callback.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y los atributos de uso [**\[ cadena \]**](string.md), [**\[ omisión \]**](ignore.md)y [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="f5c61-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="f5c61-112">Varios atributos deben estar separados por comas.</span><span class="sxs-lookup"><span data-stu-id="f5c61-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-113">*function-declarator*</span><span class="sxs-lookup"><span data-stu-id="f5c61-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-114">Especifica el especificador de tipo, el nombre de función y la lista de parámetros para la función.</span><span class="sxs-lookup"><span data-stu-id="f5c61-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-115">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="f5c61-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-116">Especifica un **tipo \_ base**, un [**\[ struct \]**](struct.md), una [**Unión**](union.md)o un tipo de [**\[ enumeración \]**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="f5c61-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="f5c61-117">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="f5c61-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-118">*declarador de puntero*</span><span class="sxs-lookup"><span data-stu-id="f5c61-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-119">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="f5c61-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="f5c61-120">Un declarador de puntero es el mismo que un declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**\[ const \]**](const.md).</span><span class="sxs-lookup"><span data-stu-id="f5c61-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-121">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="f5c61-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-122">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="f5c61-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-123">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f5c61-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-124">Especifica cero o más atributos adecuados para el tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f5c61-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="f5c61-125">Los atributos de parámetro con el atributo in también pueden sacar el [**\[ atributo \] direccional; los**](out-idl.md)atributos [**\[ \] de**](in.md) campo [**\[ primero \_ \] son**](first-is.md), [**\[ Last \_ es \]**](last-is.md), [**\[ length \_ \]**](length-is.md)es, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)y [**\[ Switch \_ Type \]**](switch-type.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y el [**\[ \_ identificador \] de contexto**](context-handle.md) y la [**\[ cadena \]**](string.md)de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="f5c61-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="f5c61-126">El atributo de uso [**\[ Ignore \]**](ignore.md) no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f5c61-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="f5c61-127">Varios atributos deben estar separados por comas.</span><span class="sxs-lookup"><span data-stu-id="f5c61-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="f5c61-128">*clara*</span><span class="sxs-lookup"><span data-stu-id="f5c61-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c61-129">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="f5c61-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="f5c61-130">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**\[ matrices \]**](../rpc/arrays.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="f5c61-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="f5c61-131">El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.</span><span class="sxs-lookup"><span data-stu-id="f5c61-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5c61-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5c61-132">Remarks</span></span>

<span data-ttu-id="f5c61-133">El atributo **\[ Anotate \]** permite reemplazar las anotaciones sal generadas por MIDL o agregarlas en lugares donde MIDL no genera explícitamente una anotación.</span><span class="sxs-lookup"><span data-stu-id="f5c61-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="f5c61-134">Si [**/sal**](-sal.md) no se especifica en la línea de comandos, se omite este atributo.</span><span class="sxs-lookup"><span data-stu-id="f5c61-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5c61-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5c61-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c61-136">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f5c61-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f5c61-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="f5c61-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="f5c61-138">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="f5c61-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 