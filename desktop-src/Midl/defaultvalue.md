---
title: defaultvalue (atributo)
description: El atributo \ DefaultValue \ le permite especificar un valor predeterminado para un parámetro opcional con tipo.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- DefaultValue (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358922"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="14b8e-104">defaultvalue (atributo)</span><span class="sxs-lookup"><span data-stu-id="14b8e-104">defaultvalue attribute</span></span>

<span data-ttu-id="14b8e-105">El atributo **\[ DefaultValue \]** permite especificar un valor predeterminado para un parámetro opcional con tipo.</span><span class="sxs-lookup"><span data-stu-id="14b8e-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="14b8e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14b8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b8e-107">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="14b8e-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-108">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="14b8e-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="14b8e-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-110">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="14b8e-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-111">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="14b8e-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-112">Especifica el nombre de la función a la que se aplicará el atributo **\[ DefaultValue \]** .</span><span class="sxs-lookup"><span data-stu-id="14b8e-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-113">*lista de parámetros obligatorios*</span><span class="sxs-lookup"><span data-stu-id="14b8e-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-114">Especifica en o más parámetros necesarios.</span><span class="sxs-lookup"><span data-stu-id="14b8e-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-115">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="14b8e-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-116">Especifica una lista de uno o varios atributos, separados por comas, que se aplican al parámetro.</span><span class="sxs-lookup"><span data-stu-id="14b8e-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-117">*tipo de parámetro*</span><span class="sxs-lookup"><span data-stu-id="14b8e-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-118">Indica el tipo del parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="14b8e-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-119">*param: nombre*</span><span class="sxs-lookup"><span data-stu-id="14b8e-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-120">Especifica el nombre del parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="14b8e-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="14b8e-121">*opcional-param-List*</span><span class="sxs-lookup"><span data-stu-id="14b8e-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14b8e-122">Especifica cero o más parámetros adicionales, cada uno de los cuales debe tener un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="14b8e-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14b8e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14b8e-123">Remarks</span></span>

<span data-ttu-id="14b8e-124">El valor predeterminado que se especifica para el parámetro puede ser cualquier constante, o una expresión que se resuelve como una constante, que se puede representar mediante una **variante**.</span><span class="sxs-lookup"><span data-stu-id="14b8e-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="14b8e-125">En concreto, no se puede aplicar el atributo **\[ \] DefaultValue** a un parámetro que sea una estructura, una matriz o un tipo **SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="14b8e-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="14b8e-126">El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):</span><span class="sxs-lookup"><span data-stu-id="14b8e-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="14b8e-127">Parámetros obligatorios (parámetros que no tienen los atributos **\[ DefaultValue \]** u **\[** [**opcional**](optional.md) **\]** ),</span><span class="sxs-lookup"><span data-stu-id="14b8e-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="14b8e-128">parámetros opcionales con o sin el atributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="14b8e-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="14b8e-129">parámetros con el atributo **\[ opcional \]** y sin el atributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="14b8e-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="14b8e-130">**\[** parámetro [**LCID**](lcid.md) **\]** , si existe,</span><span class="sxs-lookup"><span data-stu-id="14b8e-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="14b8e-131">**\[**[**retval**](retval.md) **\]** parámetro</span><span class="sxs-lookup"><span data-stu-id="14b8e-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="14b8e-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="14b8e-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="14b8e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="14b8e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b8e-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="14b8e-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="14b8e-135">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="14b8e-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="14b8e-136">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="14b8e-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="14b8e-137">**LCID**</span><span class="sxs-lookup"><span data-stu-id="14b8e-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="14b8e-138">**opta**</span><span class="sxs-lookup"><span data-stu-id="14b8e-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="14b8e-139">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="14b8e-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="14b8e-140">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="14b8e-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="14b8e-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="14b8e-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="14b8e-142">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="14b8e-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 