---
title: ptr (atributo)
description: El atributo \ PTR \ designa un puntero como puntero completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- atributo de PTR (MIDL)
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358862"
---
# <a name="ptr-attribute"></a><span data-ttu-id="84cff-104">ptr (atributo)</span><span class="sxs-lookup"><span data-stu-id="84cff-104">ptr attribute</span></span>

<span data-ttu-id="84cff-105">El atributo **\[ ptr \]** designa un puntero como puntero completo.</span><span class="sxs-lookup"><span data-stu-id="84cff-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="84cff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84cff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84cff-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="84cff-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-108">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="84cff-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="84cff-109">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md)o **\[ ptr \]**; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="84cff-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="84cff-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="84cff-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-111">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="84cff-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-112">Especifica un tipo [base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="84cff-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="84cff-113">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="84cff-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-114">*declarador estándar*</span><span class="sxs-lookup"><span data-stu-id="84cff-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-115">Especifica un declarador estándar de C, como un identificador, un declarador de puntero o un declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="84cff-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="84cff-116">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="84cff-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="84cff-117">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="84cff-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-118">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="84cff-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="84cff-119">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="84cff-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="84cff-120">La *lista de declaradores* consta de uno o varios declaradores separados por comas.</span><span class="sxs-lookup"><span data-stu-id="84cff-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="84cff-121">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="84cff-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-122">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="84cff-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-123">Especifica cero o más atributos de campo que se aplican al parámetro de la estructura o miembro de la Unión o de la función.</span><span class="sxs-lookup"><span data-stu-id="84cff-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="84cff-124">Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ \] ptr** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="84cff-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="84cff-125">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="84cff-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-126">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="84cff-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-127">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="84cff-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="84cff-128">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ ptr \]**; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="84cff-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-129">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="84cff-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-130">Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ptr \]** .</span><span class="sxs-lookup"><span data-stu-id="84cff-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="84cff-131">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="84cff-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="84cff-132">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="84cff-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-133">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="84cff-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="84cff-134">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="84cff-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84cff-135">Consta de cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="84cff-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="84cff-136">Los atributos [**de**](in.md) parámetro pueden tomar los atributos direccionales [**hacia y hacia afuera**](out-idl.md); los atributos de campo [**primero \_ son**](first-is.md), [**Last \_ es**](last-is.md), [**length \_**](length-is.md)es, [**Max \_ is**](max-is.md), [**size \_ is**](size-is.md)y [**Switch \_ Type**](switch-type.md); el atributo de puntero [**ref**](ref.md), [**Unique**](unique.md)o **\[ ptr \]**; y el identificador de [**contexto \_**](context-handle.md) y la [**cadena**](string.md)de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="84cff-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="84cff-137">El atributo de uso [**Ignore**](ignore.md) no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="84cff-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="84cff-138">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="84cff-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84cff-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84cff-139">Remarks</span></span>

<span data-ttu-id="84cff-140">El puntero completo designado por el atributo **\[ ptr \]** se aproxima a la funcionalidad completa del puntero del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="84cff-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="84cff-141">El puntero completo puede tener el valor **null** y puede cambiar durante la llamada de **null** a un valor distinto de **null**.</span><span class="sxs-lookup"><span data-stu-id="84cff-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="84cff-142">Otros nombres de la aplicación que admiten el alias y los ciclos pueden alcanzar el almacenamiento señalado por punteros completos.</span><span class="sxs-lookup"><span data-stu-id="84cff-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="84cff-143">Esta funcionalidad requiere más sobrecarga durante una llamada a procedimiento remoto para identificar los datos a los que hace referencia el puntero, determinar si el valor es **null** y detectar si dos punteros apuntan a los mismos datos.</span><span class="sxs-lookup"><span data-stu-id="84cff-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="84cff-144">Usar punteros completos para:</span><span class="sxs-lookup"><span data-stu-id="84cff-144">Use full pointers for:</span></span>

-   <span data-ttu-id="84cff-145">Valores devueltos remotos.</span><span class="sxs-lookup"><span data-stu-id="84cff-145">Remote return values.</span></span>
-   <span data-ttu-id="84cff-146">Punteros dobles, cuando no se conoce el tamaño de un parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="84cff-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="84cff-147">Punteros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="84cff-147">**NULL** pointers.</span></span>

<span data-ttu-id="84cff-148">Los punteros completos (y únicos) no se pueden usar para describir el tamaño de una matriz o unión porque estos punteros pueden tener el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="84cff-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="84cff-149">Esta restricción de MIDL evita un error que puede producirse cuando se utiliza un valor **null** como tamaño.</span><span class="sxs-lookup"><span data-stu-id="84cff-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="84cff-150">Se supone que los punteros de referencia y únicos no causan ningún alias de datos.</span><span class="sxs-lookup"><span data-stu-id="84cff-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="84cff-151">Un grafo dirigido obtenido al iniciarse a partir de un puntero único o de referencia y seguir solo los punteros únicos o de referencia no contiene ninguna reconvergencia ni ciclos.</span><span class="sxs-lookup"><span data-stu-id="84cff-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="84cff-152">Para evitar el alias, todos los valores de puntero deben obtenerse a partir de un puntero de entrada de la misma clase de puntero.</span><span class="sxs-lookup"><span data-stu-id="84cff-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="84cff-153">Si hay más de un puntero que apunta a la misma ubicación de memoria, todos los punteros deben ser punteros completos.</span><span class="sxs-lookup"><span data-stu-id="84cff-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="84cff-154">En algunos casos, se pueden mezclar punteros completos y únicos.</span><span class="sxs-lookup"><span data-stu-id="84cff-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="84cff-155">A un puntero completo se le puede asignar el valor de un puntero único, siempre y cuando la asignación no infrinja las restricciones sobre el cambio del valor de un puntero único.</span><span class="sxs-lookup"><span data-stu-id="84cff-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="84cff-156">Sin embargo, cuando se asigna un puntero único al valor de un puntero completo, puede producirse un alias.</span><span class="sxs-lookup"><span data-stu-id="84cff-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="84cff-157">La combinación de punteros completos y únicos puede producir el alias, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="84cff-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="84cff-158">Aunque "t->left" y "t->Right" apuntan a ubicaciones de memoria únicas, "t->Left->pdata" y "t->correcto->pdata" tienen alias.</span><span class="sxs-lookup"><span data-stu-id="84cff-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="84cff-159">Por esta razón, los algoritmos de compatibilidad con alias deben seguir todos los punteros (incluidos los punteros únicos y de referencia) que puedan llegar a un puntero completo.</span><span class="sxs-lookup"><span data-stu-id="84cff-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="84cff-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84cff-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="84cff-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="84cff-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cff-162">**matrices**</span><span class="sxs-lookup"><span data-stu-id="84cff-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="84cff-163">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="84cff-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="84cff-164">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="84cff-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="84cff-165">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="84cff-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="84cff-166">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="84cff-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="84cff-167">**const**</span><span class="sxs-lookup"><span data-stu-id="84cff-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="84cff-168">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="84cff-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="84cff-169">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="84cff-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="84cff-170">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="84cff-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="84cff-171">**asa**</span><span class="sxs-lookup"><span data-stu-id="84cff-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="84cff-172">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="84cff-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="84cff-173">**omitir**</span><span class="sxs-lookup"><span data-stu-id="84cff-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="84cff-174">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="84cff-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="84cff-175">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="84cff-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="84cff-176">**localizar**</span><span class="sxs-lookup"><span data-stu-id="84cff-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="84cff-177">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="84cff-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="84cff-178">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="84cff-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="84cff-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="84cff-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="84cff-180">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="84cff-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="84cff-181">**string**</span><span class="sxs-lookup"><span data-stu-id="84cff-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="84cff-182">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="84cff-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="84cff-183">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="84cff-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="84cff-184">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="84cff-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="84cff-185">**Unión**</span><span class="sxs-lookup"><span data-stu-id="84cff-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="84cff-186">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="84cff-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 