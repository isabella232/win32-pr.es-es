---
title: atributo personalizado
description: El atributo \ custom \ crea un atributo definido por el usuario.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- atributo personalizado MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685690"
---
# <a name="custom-attribute"></a><span data-ttu-id="83b6a-104">atributo personalizado</span><span class="sxs-lookup"><span data-stu-id="83b6a-104">custom attribute</span></span>

<span data-ttu-id="83b6a-105">El atributo **\[ personalizado \]** crea un atributo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="83b6a-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="83b6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83b6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b6a-107">*identificador de atributo*</span><span class="sxs-lookup"><span data-stu-id="83b6a-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="83b6a-108">GUID del atributo personalizado.</span><span class="sxs-lookup"><span data-stu-id="83b6a-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="83b6a-109">*atributo-valor*</span><span class="sxs-lookup"><span data-stu-id="83b6a-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="83b6a-110">Valor que contiene el atributo.</span><span class="sxs-lookup"><span data-stu-id="83b6a-110">The value that the attribute holds.</span></span> <span data-ttu-id="83b6a-111">El valor debe ser uno que se pueda colocar en un tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="83b6a-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="83b6a-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="83b6a-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="83b6a-113">Otros atributos, como **\[** [**UUID**](uuid.md) **\]** y **\[** [**HelpString**](helpstring.md) **\]** , que se aplican a este elemento.</span><span class="sxs-lookup"><span data-stu-id="83b6a-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="83b6a-114">*tipo de elemento*</span><span class="sxs-lookup"><span data-stu-id="83b6a-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="83b6a-115">El tipo de elemento al que se aplica el atributo personalizado.</span><span class="sxs-lookup"><span data-stu-id="83b6a-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="83b6a-116">Puede ser una instrucción de biblioteca, información de tipos, una variable, una función o un parámetro.</span><span class="sxs-lookup"><span data-stu-id="83b6a-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="83b6a-117">No se puede usar un atributo personalizado en un miembro de una coclase.</span><span class="sxs-lookup"><span data-stu-id="83b6a-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="83b6a-118">*nombre del elemento*</span><span class="sxs-lookup"><span data-stu-id="83b6a-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="83b6a-119">Nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="83b6a-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83b6a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83b6a-120">Remarks</span></span>

<span data-ttu-id="83b6a-121">Use el atributo **\[ personalizado \]** para definir su propio atributo.</span><span class="sxs-lookup"><span data-stu-id="83b6a-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="83b6a-122">Por ejemplo, puede crear un atributo con valores de cadena que proporcione el ProgID para una clase.</span><span class="sxs-lookup"><span data-stu-id="83b6a-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="83b6a-123">Para recuperar un valor de atributo personalizado, llame a uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="83b6a-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="83b6a-124">ITypeLib2:: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="83b6a-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="83b6a-125">ITypeInfo2:: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="83b6a-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="83b6a-126">ITypeInfo2:: GetFuncCustData (índice, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="83b6a-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="83b6a-127">ITypeInfo2:: GetVarCustData (índice, rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="83b6a-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="83b6a-128">ITypeInfo2:: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="83b6a-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="83b6a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="83b6a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b6a-130">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="83b6a-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="83b6a-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="83b6a-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="83b6a-132">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="83b6a-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="83b6a-133">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="83b6a-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="83b6a-134">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="83b6a-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="83b6a-135">**uuid**</span><span class="sxs-lookup"><span data-stu-id="83b6a-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 