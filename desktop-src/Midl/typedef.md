---
title: typedef (atributo)
description: La palabra clave typedef de IDL permite declaraciones TypeDef que son muy similares a las declaraciones typedef del lenguaje C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef (atributo) MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790006"
---
# <a name="typedef-attribute"></a><span data-ttu-id="fb42c-104">typedef (atributo)</span><span class="sxs-lookup"><span data-stu-id="fb42c-104">typedef attribute</span></span>

<span data-ttu-id="fb42c-105">La palabra clave **typedef** de IDL permite declaraciones **typedef** que son muy similares a las declaraciones **typedef** del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="fb42c-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="fb42c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb42c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb42c-107">*IDL-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fb42c-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fb42c-108">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="fb42c-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="fb42c-109">Los atributos de tipo válidos en un archivo IDL incluyen **\[** [](handle.md) **\]** el identificador, **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso, la **\[** [**\_**](context-handle.md) **\]** **\[** [**cadena**](string.md) **\]** y la **\[** [**omisión**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fb42c-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="fb42c-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="fb42c-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="fb42c-111">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="fb42c-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="fb42c-112">Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="fb42c-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="fb42c-113">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="fb42c-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="fb42c-114">La palabra clave [**const**](const.md) puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="fb42c-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="fb42c-115">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="fb42c-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fb42c-116">Especifica los declaradores MIDL estándar, como los identificadores, los declaradores de puntero y los declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="fb42c-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="fb42c-117">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="fb42c-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="fb42c-118">La *lista de declaradores* consta de uno o varios declaradores, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="fb42c-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="fb42c-119">*ACF-tipo-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="fb42c-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fb42c-120">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="fb42c-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="fb42c-121">Los atributos de tipo válidos en ACF incluyen **\[** [**asignar**](allocate.md) **\]** , **\[** [**codificar**](encode.md) **\]** y **\[** [**descodificar**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fb42c-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="fb42c-122">*nombreDeTipo*</span><span class="sxs-lookup"><span data-stu-id="fb42c-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="fb42c-123">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fb42c-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb42c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb42c-124">Remarks</span></span>

<span data-ttu-id="fb42c-125">La declaración **typedef** de IDL se amplía para que pueda asociar atributos de tipo a los tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="fb42c-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="fb42c-126">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fb42c-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="fb42c-127">La palabra clave **typedef** en ACF aplica atributos a los tipos que se definen en el archivo IDL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fb42c-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="fb42c-128">Por ejemplo, el atributo de tipo [**allocate**](allocate.md) permite personalizar la asignación y desasignación de memoria por la aplicación y el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="fb42c-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="fb42c-129">La instrucción **typedef** de ACF aparece como parte del cuerpo ACF.</span><span class="sxs-lookup"><span data-stu-id="fb42c-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="fb42c-130">Tenga en cuenta que la sintaxis de **typedef** de ACF es diferente de la sintaxis de **typedef** de IDL y la sintaxis de **typedef** del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="fb42c-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="fb42c-131">No se pueden introducir nuevos tipos en el ACF.</span><span class="sxs-lookup"><span data-stu-id="fb42c-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb42c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb42c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb42c-133">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="fb42c-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="fb42c-134">**allocate**</span><span class="sxs-lookup"><span data-stu-id="fb42c-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="fb42c-135">**matrices**</span><span class="sxs-lookup"><span data-stu-id="fb42c-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="fb42c-136">**const**</span><span class="sxs-lookup"><span data-stu-id="fb42c-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="fb42c-137">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="fb42c-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="fb42c-138">**descodificar**</span><span class="sxs-lookup"><span data-stu-id="fb42c-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="fb42c-139">**codificar**</span><span class="sxs-lookup"><span data-stu-id="fb42c-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="fb42c-140">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="fb42c-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="fb42c-141">**asa**</span><span class="sxs-lookup"><span data-stu-id="fb42c-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="fb42c-142">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="fb42c-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fb42c-143">**omitir**</span><span class="sxs-lookup"><span data-stu-id="fb42c-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="fb42c-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="fb42c-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="fb42c-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="fb42c-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="fb42c-146">**string**</span><span class="sxs-lookup"><span data-stu-id="fb42c-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="fb42c-147">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="fb42c-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="fb42c-148">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="fb42c-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="fb42c-149">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="fb42c-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="fb42c-150">**Unión**</span><span class="sxs-lookup"><span data-stu-id="fb42c-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="fb42c-151">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="fb42c-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 