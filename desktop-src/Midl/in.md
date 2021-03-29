---
title: in (atributo)
description: El atributo \ in \ indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- en el atributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791374"
---
# <a name="in-attribute"></a><span data-ttu-id="9b3c5-104">in (atributo)</span><span class="sxs-lookup"><span data-stu-id="9b3c5-104">in attribute</span></span>

<span data-ttu-id="9b3c5-105">El atributo **\[ in \]** indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="9b3c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b3c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b3c5-107">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-108">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="9b3c5-109">Los atributos de función válidos son **\[ \] callback**, **\[ \] local**, el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**, y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="9b3c5-110">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-111">Especifica un **tipo \_ base**, un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="9b3c5-112">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="9b3c5-113">*declarador de puntero*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-114">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="9b3c5-115">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="9b3c5-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b3c5-116">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-117">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="9b3c5-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-119">Especifica cero o más atributos adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="9b3c5-120">Los atributos de parámetro con el atributo in también pueden sacar el **\[ atributo \] direccional; los** atributos **\[ \] de** campo **\[ primero \_ \] son**, **\[ Last \_ es \]**, **\[ length \_ \]** es, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="9b3c5-121">El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="9b3c5-122">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9b3c5-123">*clara*</span><span class="sxs-lookup"><span data-stu-id="9b3c5-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c5-124">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="9b3c5-125">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="9b3c5-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="9b3c5-126">El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b3c5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b3c5-127">Remarks</span></span>

<span data-ttu-id="9b3c5-128">El atributo **\[ in \]** tiene un atributo opuesto, **\[** [**out**](out-idl.md) **\]** , que indica que un parámetro se devolverá desde el procedimiento llamado al procedimiento que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="9b3c5-129">Los atributos in y **\[ out \]** se conocen como atributos **\[ de \]** parámetro direccional porque especifican la dirección en la que se pasan los parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="9b3c5-130">Un parámetro se puede definir como **\[ in \]**, **\[ out \]** o **\[ in**, **out \]**.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="9b3c5-131">El atributo **\[ in \]** identifica los parámetros cuyas referencias se calculan mediante el código auxiliar de cliente para su transmisión al servidor.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="9b3c5-132">El atributo in se aplica a un parámetro de forma predeterminada cuando no se especifica ningún atributo **\[ de \]** parámetro direccional.</span><span class="sxs-lookup"><span data-stu-id="9b3c5-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="9b3c5-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b3c5-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="9b3c5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b3c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3c5-135">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="9b3c5-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9b3c5-136">**\_asignación de usuarios de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="9b3c5-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="9b3c5-137">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="9b3c5-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 