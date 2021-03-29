---
title: ref (atributo)
description: El atributo \ Ref \ identifica un puntero de referencia. Se usa simplemente para representar un nivel de direccionamiento indirecto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- parámetro de referencia MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904535"
---
# <a name="ref-attribute"></a><span data-ttu-id="f4fb2-105">ref (atributo)</span><span class="sxs-lookup"><span data-stu-id="f4fb2-105">ref attribute</span></span>

<span data-ttu-id="f4fb2-106">El atributo **\[ ref \]** identifica un puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="f4fb2-107">Se usa simplemente para representar un nivel de direccionamiento indirecto.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="f4fb2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4fb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4fb2-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-110">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="f4fb2-111">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; los atributos de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f4fb2-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="f4fb2-112">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-113">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-114">Especifica un tipo [base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="f4fb2-115">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-116">*declarador estándar*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-117">Especifica un declarador estándar de C, como un identificador, un declarador de puntero o un declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="f4fb2-118">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="f4fb2-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-119">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-120">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="f4fb2-121">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="f4fb2-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="f4fb2-122">La *lista de declaradores* consta de uno o varios declaradores separados por comas.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="f4fb2-123">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-124">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-125">Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="f4fb2-126">Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="f4fb2-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="f4fb2-127">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-128">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-129">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="f4fb2-130">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f4fb2-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-131">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-132">Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ref \]** .</span><span class="sxs-lookup"><span data-stu-id="f4fb2-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="f4fb2-133">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="f4fb2-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-134">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-135">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f4fb2-136">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f4fb2-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fb2-137">Consta de cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="f4fb2-138">Los atributos de parámetro pueden tomar los atributos direccionales **\[** [](in.md) **\]** hacia dentro y **\[** [**hacia fuera**](out-idl.md) **\]** ; los atributos de campo **\[** [**primero \_ son**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , length is, **\[** [**\_**](length-is.md) **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** y **\[** [**Switch \_ Type**](switch-type.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el **\[** [**\_ identificador de contexto**](context-handle.md) y la **\]** **\[** [**cadena**](string.md) **\]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="f4fb2-139">El atributo de uso **\[** [**Ignore**](ignore.md) **\]** no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="f4fb2-140">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4fb2-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4fb2-141">Remarks</span></span>

<span data-ttu-id="f4fb2-142">Un atributo de puntero se puede aplicar como atributo de tipo, como un atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro. o como un atributo de función que se aplica al tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="f4fb2-143">El atributo Pointer también puede aparecer con la **\[** palabra clave [**\_ default del puntero**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f4fb2-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="f4fb2-144">Un puntero de referencia tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f4fb2-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="f4fb2-145">Siempre apunta a un almacenamiento válido; nunca tiene el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="f4fb2-146">Siempre se puede desreferenciar un puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="f4fb2-147">Nunca cambia durante una llamada.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-147">Never changes during a call.</span></span> <span data-ttu-id="f4fb2-148">Un puntero de referencia siempre apunta al mismo almacenamiento en el cliente antes y después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="f4fb2-149">No asigna memoria nueva en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="f4fb2-150">Los datos devueltos del servidor se escriben en el almacenamiento existente especificado por el valor del puntero de referencia antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="f4fb2-151">No provoca el alias.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-151">Does not cause aliasing.</span></span> <span data-ttu-id="f4fb2-152">No se puede alcanzar el almacenamiento señalado por un puntero de referencia desde cualquier otro nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="f4fb2-153">No se puede usar un puntero de referencia como el tipo de un puntero devuelto por una función.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="f4fb2-154">Si no se especifica ningún atributo para un parámetro de puntero de nivel superior, se trata como un puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="f4fb2-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="f4fb2-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f4fb2-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="f4fb2-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4fb2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fb2-157">**matrices**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-158">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="f4fb2-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="f4fb2-159">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="f4fb2-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-160">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="f4fb2-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-161">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-162">**const**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-163">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-164">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-165">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-166">**asa**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-167">**omitir**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-168">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-169">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-170">**localizar**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-171">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-172">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-174">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-175">**string**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-176">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-177">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-178">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-179">**Unión**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="f4fb2-180">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="f4fb2-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 