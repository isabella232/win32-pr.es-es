---
title: out (atributo)
description: El atributo \ out \ identifica los parámetros de puntero devueltos por el procedimiento llamado al procedimiento que realiza la llamada (desde el servidor al cliente).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- out (atributo) MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665808"
---
# <a name="out-attribute"></a><span data-ttu-id="495d0-104">out (atributo)</span><span class="sxs-lookup"><span data-stu-id="495d0-104">out attribute</span></span>

<span data-ttu-id="495d0-105">El \[  \] atributo out identifica los parámetros de puntero devueltos por el procedimiento llamado al procedimiento que realiza la llamada (desde el servidor al cliente).</span><span class="sxs-lookup"><span data-stu-id="495d0-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="495d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="495d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="495d0-107">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="495d0-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-108">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="495d0-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="495d0-109">Los atributos de función válidos son \[ [**callback**](callback.md) \] , \[ [**local**](local.md) \] ; el atributo de puntero \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] ; y los atributos de uso \[ [**cadena**](string.md) \] , \[ [**omitir**](ignore.md) \] y \[ [**\_ identificador de contexto**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="495d0-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="495d0-110">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="495d0-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-111">Especifica un [tipo \_ base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="495d0-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="495d0-112">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="495d0-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="495d0-113">*declarador de puntero*</span><span class="sxs-lookup"><span data-stu-id="495d0-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-114">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="495d0-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="495d0-115">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="495d0-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="495d0-116">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="495d0-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-117">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="495d0-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="495d0-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="495d0-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-119">Especifica cero o más atributos adecuados para un tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="495d0-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="495d0-120">Los atributos de parámetro con el \[ atributo **out** \] también pueden sacar el atributo direccional \[  \] ; los atributos de campo \[ [**primero \_ son**](first-is.md) \] , \[ [**Last \_ es**](last-is.md) \] , \[ [**length \_**](length-is.md)es \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**size \_ is**](size-is.md) \] y \[ [**Switch \_ Type**](switch-type.md) \] ; el atributo de puntero \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] ; y el \[ [**\_ identificador de contexto**](context-handle.md) y la \] \[ [**cadena**](string.md) \] de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="495d0-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="495d0-121">El atributo de uso \[ [**Ignore**](ignore.md) \] no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="495d0-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="495d0-122">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="495d0-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="495d0-123">*clara*</span><span class="sxs-lookup"><span data-stu-id="495d0-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="495d0-124">Especifica los declaradores estándar, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="495d0-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="495d0-125">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="495d0-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="495d0-126">El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.</span><span class="sxs-lookup"><span data-stu-id="495d0-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="495d0-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="495d0-127">Remarks</span></span>

<span data-ttu-id="495d0-128">El \[ atributo **out** \] indica que un parámetro que actúa como puntero y sus datos asociados en memoria se devolverán desde el procedimiento llamado al procedimiento que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="495d0-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="495d0-129">El \[ atributo **out** \] debe ser un puntero.</span><span class="sxs-lookup"><span data-stu-id="495d0-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="495d0-130">Los compiladores de DCE IDL requieren la presencia de un \* declarador de puntero explícito en la declaración del parámetro.</span><span class="sxs-lookup"><span data-stu-id="495d0-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="495d0-131">Microsoft IDL ofrece una extensión que quita este requisito y permite una matriz o un tipo de puntero definido previamente.</span><span class="sxs-lookup"><span data-stu-id="495d0-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="495d0-132">Un atributo relacionado, \[ [**en**](in.md) \] , indica que el parámetro se pasa desde el procedimiento que realiza la llamada al procedimiento llamado.</span><span class="sxs-lookup"><span data-stu-id="495d0-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="495d0-133">Los \[  \] atributos in y \[ **out** \] especifican la dirección en la que se pasan los parámetros.</span><span class="sxs-lookup"><span data-stu-id="495d0-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="495d0-134">Un parámetro puede definirse como \[ solo **en**, solo \] \[ **fuera** \] o \[ **en**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="495d0-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="495d0-135">\[  \] Se supone que un parámetro de solo salida está sin definir cuando se llama al procedimiento remoto y el servidor asigna la memoria para el objeto.</span><span class="sxs-lookup"><span data-stu-id="495d0-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="495d0-136">Dado que el puntero o los parámetros de nivel superior deben apuntar siempre a un almacenamiento válido y, por tanto, no pueden ser **null**, no se \[  \] puede aplicar out a \[ [](unique.md) \] punteros únicos o \[ [**ptr**](ptr.md) de nivel superior \] .</span><span class="sxs-lookup"><span data-stu-id="495d0-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="495d0-137">Los parámetros que son \[  \] punteros únicos o \[ **ptr** \] deben estar \[ [**en**](in.md) \] \[ los parámetros **out** o in \] .</span><span class="sxs-lookup"><span data-stu-id="495d0-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="495d0-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="495d0-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="495d0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="495d0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495d0-140">**matrices**</span><span class="sxs-lookup"><span data-stu-id="495d0-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="495d0-141">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="495d0-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="495d0-142">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="495d0-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="495d0-143">**const**</span><span class="sxs-lookup"><span data-stu-id="495d0-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="495d0-144">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="495d0-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="495d0-145">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="495d0-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="495d0-146">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="495d0-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="495d0-147">**omitir**</span><span class="sxs-lookup"><span data-stu-id="495d0-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="495d0-148">**de**</span><span class="sxs-lookup"><span data-stu-id="495d0-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="495d0-149">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="495d0-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="495d0-150">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="495d0-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="495d0-151">**localizar**</span><span class="sxs-lookup"><span data-stu-id="495d0-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="495d0-152">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="495d0-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="495d0-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="495d0-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="495d0-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="495d0-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="495d0-155">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="495d0-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="495d0-156">**string**</span><span class="sxs-lookup"><span data-stu-id="495d0-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="495d0-157">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="495d0-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="495d0-158">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="495d0-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="495d0-159">**Unión**</span><span class="sxs-lookup"><span data-stu-id="495d0-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="495d0-160">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="495d0-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 