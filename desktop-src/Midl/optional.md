---
title: optional (atributo)
description: El atributo \ Optional \ especifica un parámetro opcional para una función miembro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- parámetro opcional MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904589"
---
# <a name="optional-attribute"></a><span data-ttu-id="e52e9-104">optional (atributo)</span><span class="sxs-lookup"><span data-stu-id="e52e9-104">optional attribute</span></span>

<span data-ttu-id="e52e9-105">El atributo **\[ opcional \]** especifica un parámetro opcional para una función miembro.</span><span class="sxs-lookup"><span data-stu-id="e52e9-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="e52e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e52e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e52e9-107">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="e52e9-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e52e9-108">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="e52e9-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e52e9-109">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="e52e9-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e52e9-110">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e52e9-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e52e9-111">*otros: atributos*</span><span class="sxs-lookup"><span data-stu-id="e52e9-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e52e9-112">Cero o más atributos de MIDL opcionales.</span><span class="sxs-lookup"><span data-stu-id="e52e9-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e52e9-113">*tipo de parámetro*</span><span class="sxs-lookup"><span data-stu-id="e52e9-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e52e9-114">El tipo de datos del parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="e52e9-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e52e9-115">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="e52e9-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e52e9-116">Especifica el nombre del parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="e52e9-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e52e9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e52e9-117">Remarks</span></span>

<span data-ttu-id="e52e9-118">El atributo **\[ opcional \]** solo es válido si el parámetro es de tipo **Variant** o **Variant** Â \* .</span><span class="sxs-lookup"><span data-stu-id="e52e9-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="e52e9-119">El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):</span><span class="sxs-lookup"><span data-stu-id="e52e9-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="e52e9-120">Parámetros obligatorios (parámetros que no tienen los **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** u **\[ opcional \]** ),</span><span class="sxs-lookup"><span data-stu-id="e52e9-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="e52e9-121">Parámetros opcionales con o sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,</span><span class="sxs-lookup"><span data-stu-id="e52e9-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="e52e9-122">Parámetros con el atributo **\[ opcional \]** y sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,</span><span class="sxs-lookup"><span data-stu-id="e52e9-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="e52e9-123">**\[** parámetro [**LCID**](lcid.md) **\]** , si existe,</span><span class="sxs-lookup"><span data-stu-id="e52e9-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="e52e9-124">**\[**[**retval**](retval.md) **\]** parámetro</span><span class="sxs-lookup"><span data-stu-id="e52e9-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="e52e9-125">No se puede aplicar el atributo **\[ opcional \]** a un parámetro que también tenga los **\[** atributos [**LCID**](lcid.md) **\]** o **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e52e9-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="e52e9-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e52e9-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="e52e9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e52e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52e9-128">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="e52e9-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="e52e9-129">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="e52e9-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e52e9-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="e52e9-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="e52e9-131">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e52e9-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e52e9-132">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e52e9-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e52e9-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="e52e9-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 