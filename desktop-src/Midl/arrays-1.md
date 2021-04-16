---
title: arrays (atributo)
description: Las matrices son colecciones homogéneas de datos a los que tiene acceso un número de índice o elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- matrices (atributo) MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685630"
---
# <a name="arrays-attribute"></a><span data-ttu-id="bd69b-104">arrays (atributo)</span><span class="sxs-lookup"><span data-stu-id="bd69b-104">arrays attribute</span></span>

<span data-ttu-id="bd69b-105">Las matrices son colecciones homogéneas de datos a los que tiene acceso un número de índice o elemento.</span><span class="sxs-lookup"><span data-stu-id="bd69b-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="bd69b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd69b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd69b-107">*Type-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="bd69b-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-108">Especifica cero o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="bd69b-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="bd69b-109">Entre los atributos de tipo válidos se incluyen el [**\[ \] identificador**](handle.md), el [**\[ \_ \] tipo de conmutador**](switch-type.md), la [**\[ transmisión \_ como \]**](transmit-as.md); el atributo de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y el [**\[ \_ identificador \] de contexto**](context-handle.md)de los atributos de uso, [**\[ String \]**](string.md)y [**\[ Ignore \]**](ignore.md).</span><span class="sxs-lookup"><span data-stu-id="bd69b-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="bd69b-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="bd69b-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-111">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="bd69b-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-112">Especifica el identificador de tipo, tipo base, [**estructura**](struct.md), [**Unión**](union.md)o tipo de [**enumeración**](enum.md) .</span><span class="sxs-lookup"><span data-stu-id="bd69b-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="bd69b-113">La especificación de tipo puede incluir una especificación de almacenamiento opcional.</span><span class="sxs-lookup"><span data-stu-id="bd69b-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-114">*puntero-decl*</span><span class="sxs-lookup"><span data-stu-id="bd69b-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-115">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="bd69b-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="bd69b-116">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C, construido a partir del **\*** designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="bd69b-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-117">*array-declarator*</span><span class="sxs-lookup"><span data-stu-id="bd69b-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-118">Especifica el nombre de la matriz, seguido de una de las construcciones siguientes para cada dimensión de la matriz: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" o "**\[ ***Lower...*** Upper \]**", donde *inferior* y *superior* son valores constantes que representan los límites inferior y superior.</span><span class="sxs-lookup"><span data-stu-id="bd69b-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="bd69b-119">La constante *inferior* debe evaluarse como cero.</span><span class="sxs-lookup"><span data-stu-id="bd69b-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-120">*etiqueta*</span><span class="sxs-lookup"><span data-stu-id="bd69b-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-121">Especifica una etiqueta opcional para la estructura o Unión.</span><span class="sxs-lookup"><span data-stu-id="bd69b-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-122">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="bd69b-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-123">Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="bd69b-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="bd69b-124">Entre los atributos de campo válidos se incluyen [**\[ First \_ \] es**](first-is.md), [**\[ Last \_ \] es**](last-is.md), [**\[ length \_ \]**](length-is.md)is, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ es \]**](size-is.md); la [**\[ cadena \]**](string.md)de atributos de uso y [**\[ Ignore \]**](ignore.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)y [**\[ ptr \]**](ptr.md); y el [**\[ \_ tipo \] de modificador**](switch-type.md)de atributo Union.</span><span class="sxs-lookup"><span data-stu-id="bd69b-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="bd69b-125">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="bd69b-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="bd69b-126">Tenga en cuenta que los atributos enumerados anteriormente, **\[ First \_ \] is**, **\[ Last \_ is \]** y [**\[ Ignore \]**](ignore.md) no son válidos para uniones.</span><span class="sxs-lookup"><span data-stu-id="bd69b-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-127">*Limited-Expression*</span><span class="sxs-lookup"><span data-stu-id="bd69b-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-128">Especifica una expresión del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="bd69b-128">Specifies a C-language expression.</span></span> <span data-ttu-id="bd69b-129">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="bd69b-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="bd69b-130">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="bd69b-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-131">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="bd69b-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-132">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="bd69b-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="bd69b-133">Los atributos de función válidos son [**\[ callback \]**](callback.md), [**\[ \] local**](local.md); el atributo de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y la [**\[ cadena \]**](string.md)de atributos de uso, y el [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="bd69b-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-134">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="bd69b-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-135">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="bd69b-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="bd69b-136">*param-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="bd69b-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bd69b-137">Especifica los atributos direccionales y uno o varios atributos de campo opcionales que se aplican al parámetro de la matriz.</span><span class="sxs-lookup"><span data-stu-id="bd69b-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="bd69b-138">Entre los atributos de campo válidos [**\[ se incluyen Max \_ \] is**](max-is.md), [**\[ size \_ is \]**](size-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)y [**\[ Last \_ is \]**](last-is.md).</span><span class="sxs-lookup"><span data-stu-id="bd69b-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd69b-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd69b-139">Remarks</span></span>

<span data-ttu-id="bd69b-140">Las matrices de MIDL usan un estilo similar a, pero no exactamente igual que C y C++.</span><span class="sxs-lookup"><span data-stu-id="bd69b-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="bd69b-141">Para obtener más información, vea [matrices de MIDL](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="bd69b-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bd69b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd69b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd69b-143">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="bd69b-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="bd69b-144">**const**</span><span class="sxs-lookup"><span data-stu-id="bd69b-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="bd69b-145">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="bd69b-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="bd69b-146">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="bd69b-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="bd69b-147">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="bd69b-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="bd69b-148">**asa**</span><span class="sxs-lookup"><span data-stu-id="bd69b-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="bd69b-149">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="bd69b-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bd69b-150">**omitir**</span><span class="sxs-lookup"><span data-stu-id="bd69b-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="bd69b-151">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="bd69b-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="bd69b-152">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="bd69b-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="bd69b-153">**localizar**</span><span class="sxs-lookup"><span data-stu-id="bd69b-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="bd69b-154">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="bd69b-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="bd69b-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="bd69b-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="bd69b-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="bd69b-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="bd69b-157">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="bd69b-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="bd69b-158">**string**</span><span class="sxs-lookup"><span data-stu-id="bd69b-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="bd69b-159">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="bd69b-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="bd69b-160">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="bd69b-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="bd69b-161">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="bd69b-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="bd69b-162">**Unión**</span><span class="sxs-lookup"><span data-stu-id="bd69b-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="bd69b-163">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="bd69b-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




