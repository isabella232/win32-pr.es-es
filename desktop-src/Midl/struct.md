---
title: struct (atributo)
description: La palabra clave struct se usa en un especificador de tipo de estructura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- atributo de estructura MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665807"
---
# <a name="struct-attribute"></a><span data-ttu-id="dfba3-104">struct (atributo)</span><span class="sxs-lookup"><span data-stu-id="dfba3-104">struct attribute</span></span>

<span data-ttu-id="dfba3-105">La palabra clave **struct** se usa en un especificador de tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="dfba3-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="dfba3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfba3-107">*struct: etiqueta*</span><span class="sxs-lookup"><span data-stu-id="dfba3-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="dfba3-108">Especifica una etiqueta opcional para la estructura.</span><span class="sxs-lookup"><span data-stu-id="dfba3-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="dfba3-109">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="dfba3-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dfba3-110">Especifica cero o más atributos de campo que se aplican al miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="dfba3-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="dfba3-111">Entre los atributos de campo válidos **\[** [**se incluyen First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)is **\]** , **\[** [**Max \_ is**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; la cadena de atributos de uso **\[** [](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="dfba3-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="dfba3-112">Separe varios atributos de campo con comas.</span><span class="sxs-lookup"><span data-stu-id="dfba3-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="dfba3-113">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="dfba3-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="dfba3-114">Especifica un tipo [base](midl-base-types.md), un **struct**, una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="dfba3-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="dfba3-115">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="dfba3-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="dfba3-116">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="dfba3-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dfba3-117">Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="dfba3-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="dfba3-118">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="dfba3-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="dfba3-119">Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="dfba3-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfba3-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfba3-120">Remarks</span></span>

<span data-ttu-id="dfba3-121">El especificador de tipo de estructura IDL, **struct**, difiere del especificador de tipo C estándar de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfba3-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="dfba3-122">Cada miembro de la estructura puede asociarse a atributos de campo opcionales que describen las características de ese miembro de estructura para los fines de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="dfba3-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="dfba3-123">Los campos de bits y los declaradores de función no se permiten en estructuras que se utilizan en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="dfba3-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="dfba3-124">Estas construcciones de declarador de C estándar solo se pueden usar si la estructura no se transmite en la red.</span><span class="sxs-lookup"><span data-stu-id="dfba3-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="dfba3-125">La forma de las estructuras debe ser la misma en todas las plataformas para garantizar la interconectividad.</span><span class="sxs-lookup"><span data-stu-id="dfba3-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="dfba3-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfba3-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="dfba3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfba3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfba3-128">**matrices**</span><span class="sxs-lookup"><span data-stu-id="dfba3-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="dfba3-129">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="dfba3-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="dfba3-130">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="dfba3-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="dfba3-131">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="dfba3-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="dfba3-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="dfba3-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="dfba3-133">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="dfba3-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="dfba3-134">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="dfba3-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="dfba3-135">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="dfba3-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="dfba3-136">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="dfba3-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dfba3-137">**omitir**</span><span class="sxs-lookup"><span data-stu-id="dfba3-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="dfba3-138">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="dfba3-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="dfba3-139">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="dfba3-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="dfba3-140">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="dfba3-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="dfba3-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="dfba3-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="dfba3-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="dfba3-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="dfba3-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="dfba3-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="dfba3-144">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="dfba3-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="dfba3-145">**string**</span><span class="sxs-lookup"><span data-stu-id="dfba3-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="dfba3-146">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="dfba3-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="dfba3-147">**Unión**</span><span class="sxs-lookup"><span data-stu-id="dfba3-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="dfba3-148">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="dfba3-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 