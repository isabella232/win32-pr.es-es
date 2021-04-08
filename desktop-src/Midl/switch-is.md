---
title: switch_is (atributo)
description: El atributo \ switch \_ es \ especifica la expresión o el identificador que actúa como discriminante de Unión que selecciona el miembro de Unión.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is el atributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994734"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="c4f25-104">el modificador \_ es un atributo</span><span class="sxs-lookup"><span data-stu-id="c4f25-104">switch\_is attribute</span></span>

<span data-ttu-id="c4f25-105">El atributo **\[ Switch \_ es \]** especifica la expresión o el identificador que actúa como discriminante de Unión que selecciona el miembro de Unión.</span><span class="sxs-lookup"><span data-stu-id="c4f25-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="c4f25-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4f25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f25-107">*struct: etiqueta*</span><span class="sxs-lookup"><span data-stu-id="c4f25-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-108">Especifica una etiqueta opcional para una estructura.</span><span class="sxs-lookup"><span data-stu-id="c4f25-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-109">*Limited-expr*</span><span class="sxs-lookup"><span data-stu-id="c4f25-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-110">Especifica una expresión de lenguaje C admitida por MIDL.</span><span class="sxs-lookup"><span data-stu-id="c4f25-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="c4f25-111">Se admiten casi todas las expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="c4f25-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="c4f25-112">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="c4f25-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="c4f25-113">MIDL no permite las invocaciones de función en expresiones y no permite operadores de incremento previo y posterior y de decremento anterior y posterior.</span><span class="sxs-lookup"><span data-stu-id="c4f25-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-114">*Field-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="c4f25-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-115">Especifica cero o más atributos de campo que se aplican a un miembro de Unión.</span><span class="sxs-lookup"><span data-stu-id="c4f25-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="c4f25-116">Entre los atributos de campo válidos **\[** [**se incluyen First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , length es, **\[** [**\_**](length-is.md) **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y para miembros que son uniones, el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="c4f25-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="c4f25-117">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="c4f25-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-118">*Union-Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="c4f25-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-119">Especifica el identificador de tipo de [**Unión**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="c4f25-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="c4f25-120">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="c4f25-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-121">*declarador y lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="c4f25-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-122">Especifica un declarador estándar de C, como un identificador, un declarador de puntero y un declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="c4f25-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="c4f25-123">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las uniones que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="c4f25-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="c4f25-124">Estos declaradores se permiten en las uniones que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="c4f25-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-125">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="c4f25-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-126">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="c4f25-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="c4f25-127">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="c4f25-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-128">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="c4f25-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-129">Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="c4f25-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="c4f25-130">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="c4f25-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-131">*declarador de puntero*</span><span class="sxs-lookup"><span data-stu-id="c4f25-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-132">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="c4f25-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="c4f25-133">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="c4f25-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-134">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="c4f25-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-135">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="c4f25-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-136">*param-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="c4f25-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-137">Especifica cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="c4f25-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="c4f25-138">Los atributos de parámetro pueden tomar los atributos direccionales hacia arriba y **\[ hacia \] fuera**, los atributos **\[ \] de** campo **\[ primero \_ son \]**, **\[ Last \_ es \]**, **\[ length \_ \]** is, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="c4f25-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="c4f25-139">El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4f25-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="c4f25-140">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="c4f25-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c4f25-141">*tipo de Unión*</span><span class="sxs-lookup"><span data-stu-id="c4f25-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f25-142">Identifica el especificador de tipo de [**Unión**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="c4f25-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4f25-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4f25-143">Remarks</span></span>

<span data-ttu-id="c4f25-144">El discriminante asociado con el **\[ modificador \_ es \]** el atributo debe definirse en el mismo nivel lógico que la Unión:</span><span class="sxs-lookup"><span data-stu-id="c4f25-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="c4f25-145">Cuando la Unión es un parámetro, el discriminante de Unión debe ser otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4f25-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="c4f25-146">Cuando la Unión es un campo de una estructura, discriminante debe ser otro campo de la misma estructura.</span><span class="sxs-lookup"><span data-stu-id="c4f25-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="c4f25-147">La secuencia de una estructura o una lista de parámetros de función no es significativa.</span><span class="sxs-lookup"><span data-stu-id="c4f25-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="c4f25-148">La Unión puede preceder o seguir discriminante.</span><span class="sxs-lookup"><span data-stu-id="c4f25-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="c4f25-149">El atributo **\[ Switch \_ es \]** puede aparecer como atributo de campo o como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4f25-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="c4f25-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c4f25-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="c4f25-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4f25-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f25-152">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="c4f25-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c4f25-153">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="c4f25-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="c4f25-154">**const**</span><span class="sxs-lookup"><span data-stu-id="c4f25-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c4f25-155">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="c4f25-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="c4f25-156">Uniones encapsuladas</span><span class="sxs-lookup"><span data-stu-id="c4f25-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="c4f25-157">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="c4f25-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="c4f25-158">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="c4f25-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="c4f25-159">**omitir**</span><span class="sxs-lookup"><span data-stu-id="c4f25-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="c4f25-160">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="c4f25-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="c4f25-161">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="c4f25-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="c4f25-162">**localizar**</span><span class="sxs-lookup"><span data-stu-id="c4f25-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="c4f25-163">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="c4f25-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="c4f25-164">Uniones no encapsuladas</span><span class="sxs-lookup"><span data-stu-id="c4f25-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="c4f25-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c4f25-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c4f25-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="c4f25-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c4f25-167">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="c4f25-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="c4f25-168">**string**</span><span class="sxs-lookup"><span data-stu-id="c4f25-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="c4f25-169">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="c4f25-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="c4f25-170">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="c4f25-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="c4f25-171">**Unión**</span><span class="sxs-lookup"><span data-stu-id="c4f25-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="c4f25-172">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="c4f25-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




