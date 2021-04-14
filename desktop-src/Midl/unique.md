---
title: unique (atributo)
description: El atributo \ Unique \ especifica un puntero único.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- único atributo MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665781"
---
# <a name="unique-attribute"></a><span data-ttu-id="67b5d-104">unique (atributo)</span><span class="sxs-lookup"><span data-stu-id="67b5d-104">unique attribute</span></span>

<span data-ttu-id="67b5d-105">El atributo **\[ Unique \]** especifica un puntero único.</span><span class="sxs-lookup"><span data-stu-id="67b5d-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="67b5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b5d-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="67b5d-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-108">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="67b5d-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="67b5d-109">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="67b5d-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="67b5d-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="67b5d-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-111">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="67b5d-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-112">Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="67b5d-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="67b5d-113">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="67b5d-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-114">*declarador y lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="67b5d-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-115">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="67b5d-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="67b5d-116">Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="67b5d-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="67b5d-117">La *lista de declaradores* consta de uno o varios declaradores separados por comas.</span><span class="sxs-lookup"><span data-stu-id="67b5d-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="67b5d-118">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="67b5d-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-119">*struct-or-Union-declarator*</span><span class="sxs-lookup"><span data-stu-id="67b5d-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-120">Especifica un [**destructor**](struct.md) o un declarador de [**Unión**](union.md) de MIDL.</span><span class="sxs-lookup"><span data-stu-id="67b5d-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-121">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="67b5d-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-122">Especifica cero o más atributos de campo que se aplican al miembro de estructura, miembro de unión o parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="67b5d-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="67b5d-123">Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[ \] cadena**, **\[ \] omitir** y **\[ \_ \] identificador de contexto**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** y el **\[ \_ tipo \] de modificador** de atributo Union.</span><span class="sxs-lookup"><span data-stu-id="67b5d-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="67b5d-124">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="67b5d-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-125">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="67b5d-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-126">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="67b5d-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="67b5d-127">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="67b5d-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-128">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="67b5d-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-129">Especifica al menos un declarador de puntero al que se aplica el atributo **\[ único \]** .</span><span class="sxs-lookup"><span data-stu-id="67b5d-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="67b5d-130">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="67b5d-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-131">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="67b5d-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-132">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="67b5d-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="67b5d-133">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="67b5d-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="67b5d-134">Consta de cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="67b5d-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="67b5d-135">Los atributos **\[ de \]** parámetro pueden tomar los atributos direccionales hacia dentro y **\[ hacia \] fuera**; los atributos de campo **\[ primero \_ son \]**, **\[ Last \_ es \]**, **\[ length \_ \]** is, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **Unique** o [**ptr**](ptr.md); y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="67b5d-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="67b5d-136">El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="67b5d-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="67b5d-137">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="67b5d-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67b5d-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67b5d-138">Remarks</span></span>

<span data-ttu-id="67b5d-139">Los atributos de puntero se pueden aplicar como un atributo de tipo. como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="67b5d-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="67b5d-140">El atributo Pointer también puede aparecer con la **\[** palabra clave [**\_ default del puntero**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="67b5d-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="67b5d-141">Un puntero único tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="67b5d-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="67b5d-142">Puede tener el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="67b5d-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="67b5d-143">Puede cambiar durante una llamada de **null** a un valor **distinto de NULL, de** un valor distinto de **null** a **null** o de un valor distinto de **null** a otro.</span><span class="sxs-lookup"><span data-stu-id="67b5d-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="67b5d-144">Puede asignar memoria nueva en el cliente.</span><span class="sxs-lookup"><span data-stu-id="67b5d-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="67b5d-145">Cuando el puntero único cambia de **null** a no **null**, los datos devueltos del servidor se escriben en el nuevo almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="67b5d-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="67b5d-146">Puede utilizar la memoria existente en el cliente sin asignar memoria nueva.</span><span class="sxs-lookup"><span data-stu-id="67b5d-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="67b5d-147">Cuando un puntero único cambia durante una llamada de un valor distinto de **null** a otro, se supone que el puntero apunta a un objeto de datos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="67b5d-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="67b5d-148">Los datos devueltos del servidor se escriben en el almacenamiento existente especificado por el valor del puntero único antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="67b5d-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="67b5d-149">Puede haber memoria huérfana en el cliente.</span><span class="sxs-lookup"><span data-stu-id="67b5d-149">Can orphan memory on the client.</span></span> <span data-ttu-id="67b5d-150">La memoria a la que hace referencia un puntero único no **nulo** nunca se puede liberar si el puntero único cambia a **null** durante una llamada y el cliente no tiene otro medio para desreferenciar el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="67b5d-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="67b5d-151">No provoca el alias.</span><span class="sxs-lookup"><span data-stu-id="67b5d-151">Does not cause aliasing.</span></span> <span data-ttu-id="67b5d-152">Al igual que el almacenamiento señalado por un puntero de referencia, no se puede alcanzar el almacenamiento señalado por un puntero único desde cualquier otro nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="67b5d-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="67b5d-153">El código auxiliar llama a las funciones de administración de memoria proporcionadas por el usuario [**MIDL \_ \_ asignar**](/windows/desktop/Rpc/the-midl-user-allocate-function) y [**\_ \_ liberar**](/windows/desktop/Rpc/the-midl-user-free-function) al usuario de MIDL para asignar y desasignar la memoria necesaria para los punteros únicos y sus correspondientes.</span><span class="sxs-lookup"><span data-stu-id="67b5d-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="67b5d-154">Las restricciones siguientes se aplican a los punteros únicos:</span><span class="sxs-lookup"><span data-stu-id="67b5d-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="67b5d-155">El atributo **\[ Unique \]** no se puede aplicar a los parámetros de identificador de enlace ( [**Handle \_ t**](handle-t.md)) y de identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="67b5d-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="67b5d-156">El atributo **\[ Unique \]** no se puede aplicar a **\[** [](out-idl.md) **\]** parámetros de puntero de nivel superior solo out (parámetros que solo tienen el atributo Direction de **\[ salida \]** ).</span><span class="sxs-lookup"><span data-stu-id="67b5d-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="67b5d-157">De forma predeterminada, los punteros de nivel superior de las listas de parámetros son **\[** [](ref.md) **\]** punteros de referencia.</span><span class="sxs-lookup"><span data-stu-id="67b5d-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="67b5d-158">Esto es así incluso si la interfaz especifica **el \_ valor predeterminado del puntero (único)**.</span><span class="sxs-lookup"><span data-stu-id="67b5d-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="67b5d-159">Los parámetros de nivel superior de las listas de parámetros deben especificarse con el atributo **\[ Unique \]** como un puntero único.</span><span class="sxs-lookup"><span data-stu-id="67b5d-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="67b5d-160">No se pueden usar punteros únicos para describir el tamaño de una matriz o un brazo de Unión porque los punteros únicos pueden tener el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="67b5d-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="67b5d-161">Esta restricción evita el error que se produce si se usa un valor **null** como tamaño de la matriz o el tamaño de la Unión-ARM.</span><span class="sxs-lookup"><span data-stu-id="67b5d-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="67b5d-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67b5d-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="67b5d-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="67b5d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b5d-164">**matrices**</span><span class="sxs-lookup"><span data-stu-id="67b5d-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="67b5d-165">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="67b5d-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="67b5d-166">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="67b5d-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="67b5d-167">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="67b5d-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="67b5d-168">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="67b5d-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="67b5d-169">**const**</span><span class="sxs-lookup"><span data-stu-id="67b5d-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="67b5d-170">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="67b5d-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="67b5d-171">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="67b5d-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="67b5d-172">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="67b5d-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="67b5d-173">**asa**</span><span class="sxs-lookup"><span data-stu-id="67b5d-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="67b5d-174">**identificador \_ t**</span><span class="sxs-lookup"><span data-stu-id="67b5d-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="67b5d-175">**omitir**</span><span class="sxs-lookup"><span data-stu-id="67b5d-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="67b5d-176">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="67b5d-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="67b5d-177">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="67b5d-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="67b5d-178">**localizar**</span><span class="sxs-lookup"><span data-stu-id="67b5d-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="67b5d-179">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="67b5d-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="67b5d-180">\_asignación de usuarios de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="67b5d-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="67b5d-181">usuario de MIDL \_ \_ gratis</span><span class="sxs-lookup"><span data-stu-id="67b5d-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="67b5d-182">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="67b5d-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="67b5d-183">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="67b5d-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="67b5d-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="67b5d-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="67b5d-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="67b5d-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="67b5d-186">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="67b5d-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="67b5d-187">**string**</span><span class="sxs-lookup"><span data-stu-id="67b5d-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="67b5d-188">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="67b5d-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="67b5d-189">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="67b5d-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="67b5d-190">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="67b5d-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="67b5d-191">**Unión**</span><span class="sxs-lookup"><span data-stu-id="67b5d-191">**union**</span></span>](union.md)
</dt> </dl>

 

 