---
title: string (atributo)
description: El atributo \ String \ indica que la matriz de caracteres unidimensional, WCHAR \_ t, byte (o equivalente) o el puntero a dicha matriz se debe tratar como una cadena.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- atributo de cadena MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995205"
---
# <a name="string-attribute"></a><span data-ttu-id="e8a52-104">string (atributo)</span><span class="sxs-lookup"><span data-stu-id="e8a52-104">string attribute</span></span>

<span data-ttu-id="e8a52-105">El atributo de **\[ cadena \]** indica que la matriz de [**caracteres**](char-idl.md)unidimensional, [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o el puntero a una matriz de este tipo se deben tratar como una cadena.</span><span class="sxs-lookup"><span data-stu-id="e8a52-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="e8a52-106">La cadena también puede ser una matriz (o un puntero a una matriz) de construcciones cuyos campos son todo el tipo **byte**.</span><span class="sxs-lookup"><span data-stu-id="e8a52-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="e8a52-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8a52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a52-108">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="e8a52-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-109">Especifica uno o más atributos que se aplican a un tipo.</span><span class="sxs-lookup"><span data-stu-id="e8a52-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="e8a52-110">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[ String \]** y **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e8a52-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="e8a52-111">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="e8a52-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-112">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="e8a52-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-113">Especifica un [tipo base](midl-base-types.md), un tipo de [**estructura**](struct.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="e8a52-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="e8a52-114">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="e8a52-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-115">*declarador estándar*</span><span class="sxs-lookup"><span data-stu-id="e8a52-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-116">Especifica un declarador estándar de C, como un identificador, un declarador de puntero o un declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="e8a52-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="e8a52-117">Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e8a52-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-118">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="e8a52-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-119">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="e8a52-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e8a52-120">Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e8a52-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e8a52-121">La *lista de declaradores* consta de uno o varios declaradores separados por comas.</span><span class="sxs-lookup"><span data-stu-id="e8a52-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="e8a52-122">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="e8a52-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-123">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="e8a52-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-124">Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="e8a52-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="e8a52-125">Los dos atributos de campo válidos son **\[** [**Max \_ is**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[ \] cadena**, **\[ \] omitir** y **\[ \_ \] identificador de contexto**, el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** y el **\[ \_ tipo \] de modificador** de atributo Union.</span><span class="sxs-lookup"><span data-stu-id="e8a52-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="e8a52-126">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="e8a52-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-127">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="e8a52-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-128">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="e8a52-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e8a52-129">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="e8a52-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-130">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="e8a52-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-131">Especifica un declarador de puntero opcional al que se aplica el atributo de **\[ cadena \]** .</span><span class="sxs-lookup"><span data-stu-id="e8a52-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="e8a52-132">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="e8a52-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-133">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="e8a52-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-134">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="e8a52-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e8a52-135">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e8a52-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a52-136">Consta de cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="e8a52-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="e8a52-137">Los atributos **\[ de \]** parámetro pueden tomar los atributos direccionales **\[ hacia y hacia afuera \]**; los atributos de campo **\[** [**Max \_ es**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; el atributo de puntero **\[ \] ref**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="e8a52-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="e8a52-138">El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="e8a52-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="e8a52-139">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="e8a52-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8a52-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8a52-140">Remarks</span></span>

<span data-ttu-id="e8a52-141">Si el atributo de **\[ \] cadena** se utiliza con una matriz cuyos límites se determinan en tiempo de ejecución, también debe especificar **\[ \_ \]** un atributo size o **\[ Max \_ is \]** , como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e8a52-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="e8a52-142">El atributo de **\[ cadena \]** no se puede usar con atributos que especifican el intervalo de elementos transmitidos, como **\[ First \_ es \]**, **\[ Last \_ es \]** y **\[ length \_ es \]**.</span><span class="sxs-lookup"><span data-stu-id="e8a52-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="e8a52-143">Cuando se usa en matrices multidimensionales, el atributo de **\[ cadena \]** se aplica a la matriz situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="e8a52-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="e8a52-144">Para definir una cadena contada, no use el atributo de **\[ cadena \]** .</span><span class="sxs-lookup"><span data-stu-id="e8a52-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="e8a52-145">Use una matriz de caracteres o un puntero basado en caracteres como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="e8a52-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="e8a52-146">El atributo de **\[ cadena \]** especifica que el código auxiliar debe utilizar un método proporcionado por el lenguaje para determinar la longitud de las cadenas.</span><span class="sxs-lookup"><span data-stu-id="e8a52-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="e8a52-147">Al declarar cadenas en C, debe asignar espacio para un carácter adicional que marca el final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e8a52-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="e8a52-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8a52-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="e8a52-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8a52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a52-150">**matrices**</span><span class="sxs-lookup"><span data-stu-id="e8a52-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e8a52-151">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="e8a52-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e8a52-152">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="e8a52-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e8a52-153">**char**</span><span class="sxs-lookup"><span data-stu-id="e8a52-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e8a52-154">**const**</span><span class="sxs-lookup"><span data-stu-id="e8a52-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e8a52-155">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="e8a52-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e8a52-156">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="e8a52-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e8a52-157">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="e8a52-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e8a52-158">**asa**</span><span class="sxs-lookup"><span data-stu-id="e8a52-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="e8a52-159">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="e8a52-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e8a52-160">**omitir**</span><span class="sxs-lookup"><span data-stu-id="e8a52-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e8a52-161">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="e8a52-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e8a52-162">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="e8a52-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e8a52-163">**localizar**</span><span class="sxs-lookup"><span data-stu-id="e8a52-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e8a52-164">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="e8a52-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e8a52-165">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="e8a52-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="e8a52-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e8a52-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e8a52-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="e8a52-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e8a52-168">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="e8a52-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e8a52-169">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="e8a52-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e8a52-170">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="e8a52-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e8a52-171">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="e8a52-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="e8a52-172">**Unión**</span><span class="sxs-lookup"><span data-stu-id="e8a52-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e8a52-173">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="e8a52-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="e8a52-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="e8a52-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 