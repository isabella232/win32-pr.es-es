---
title: descodificar atributo
description: El atributo \ decode \ ACF especifica que un procedimiento o un tipo necesita compatibilidad de deserialización.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- descodificar el atributo MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358897"
---
# <a name="decode-attribute"></a><span data-ttu-id="7cb7a-104">descodificar atributo</span><span class="sxs-lookup"><span data-stu-id="7cb7a-104">decode attribute</span></span>

<span data-ttu-id="7cb7a-105">El atributo **\[ Decode \]** ACF especifica que un procedimiento o un tipo necesita compatibilidad de deserialización.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="7cb7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cb7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb7a-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-108">Especifica otros atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-109">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-110">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-111">*definición de interfaz*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-112">Especifica las instrucciones IDL que forman la definición de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-113">*OP-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-114">Especifica otros atributos operativos que se aplican al procedimiento como **\[** [**encode**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cb7a-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-115">*proc: nombre*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-116">Especifica el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-118">Especifica otros atributos, como **\[** [**encode**](encode.md) **\]** y **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cb7a-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7cb7a-119">*nombre de tipo*</span><span class="sxs-lookup"><span data-stu-id="7cb7a-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb7a-120">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cb7a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cb7a-121">Remarks</span></span>

<span data-ttu-id="7cb7a-122">El atributo **\[ Decode \]** hace que el compilador MIDL genere código que una aplicación puede utilizar para recuperar datos serializados de un búfer.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="7cb7a-123">El **\[** atributo [**encode**](encode.md) **\]** proporciona compatibilidad de serialización y genera el código para serializar los datos en un búfer.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="7cb7a-124">Use los **\[** atributos [**encode**](encode.md) **\]** y **\[ Decode \]** en un ACF para generar código de serialización para los procedimientos o tipos definidos en el archivo IDL de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="7cb7a-125">Cuando se usa como atributo de interfaz, **\[ descodificar \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="7cb7a-126">Cuando se usa como atributo de tipo, **\[ descodificar \]** solo se aplica al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="7cb7a-127">Cuando se usa como atributo operativo, **\[ descodificar \]** solo se aplica a ese procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7cb7a-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="7cb7a-128">Para obtener más información sobre el uso de esta compatibilidad de serialización, vea [servicios de serialización](/windows/desktop/Rpc/serialization-services) y **\[** [**codificación**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cb7a-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cb7a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cb7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb7a-130">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="7cb7a-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="7cb7a-131">**allocate**</span><span class="sxs-lookup"><span data-stu-id="7cb7a-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="7cb7a-132">**codificar**</span><span class="sxs-lookup"><span data-stu-id="7cb7a-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 