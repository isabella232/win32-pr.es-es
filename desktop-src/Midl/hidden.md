---
title: hidden (atributo)
description: El atributo \ Hidden \ indica que el elemento existe pero no debe mostrarse en un explorador orientado al usuario.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- MIDL de atributo oculto
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651356"
---
# <a name="hidden-attribute"></a><span data-ttu-id="e69d4-104">hidden (atributo)</span><span class="sxs-lookup"><span data-stu-id="e69d4-104">hidden attribute</span></span>

<span data-ttu-id="e69d4-105">El atributo **\[ Hidden \]** indica que el elemento existe pero no debe mostrarse en un explorador orientado al usuario.</span><span class="sxs-lookup"><span data-stu-id="e69d4-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="e69d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e69d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e69d4-107">*otros: atributos*</span><span class="sxs-lookup"><span data-stu-id="e69d4-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-108">Cero o más atributos de MIDL opcionales.</span><span class="sxs-lookup"><span data-stu-id="e69d4-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-109">*Element*</span><span class="sxs-lookup"><span data-stu-id="e69d4-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-110">Una de las siguientes directivas: [**CoClass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)o [**Library**](library.md).</span><span class="sxs-lookup"><span data-stu-id="e69d4-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-111">*nombre del elemento*</span><span class="sxs-lookup"><span data-stu-id="e69d4-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-112">El nombre que otros componentes de software pueden usar para delimitar el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="e69d4-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-113">*Figura*</span><span class="sxs-lookup"><span data-stu-id="e69d4-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-114">Especifica las instrucciones que componen la definición del elemento.</span><span class="sxs-lookup"><span data-stu-id="e69d4-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-115">*tipo de función*</span><span class="sxs-lookup"><span data-stu-id="e69d4-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-116">Tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="e69d4-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-117">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="e69d4-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-118">Nombre que se usa para invocar la función.</span><span class="sxs-lookup"><span data-stu-id="e69d4-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="e69d4-119">*opcional-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="e69d4-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e69d4-120">Cero o más parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="e69d4-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e69d4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e69d4-121">Remarks</span></span>

<span data-ttu-id="e69d4-122">El atributo **\[ Hidden \]** permite quitar miembros de la interfaz (mediante la protección del uso adicional) y mantener la compatibilidad con el código existente.</span><span class="sxs-lookup"><span data-stu-id="e69d4-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="e69d4-123">Puede usar el atributo **\[ Hidden \]** en las propiedades, los métodos y las instrucciones [**CoClass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)y [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="e69d4-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="e69d4-124">Cuando se especifica para una biblioteca, el atributo **\[ Hidden \]** evita que se muestre toda la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e69d4-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="e69d4-125">Este uso está diseñado para emplearlo con controles.</span><span class="sxs-lookup"><span data-stu-id="e69d4-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="e69d4-126">Los hosts deben crear una biblioteca de tipos que ajuste el control con propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="e69d4-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="e69d4-127">Marcas</span><span class="sxs-lookup"><span data-stu-id="e69d4-127">Flags</span></span>

<span data-ttu-id="e69d4-128">VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="e69d4-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e69d4-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="e69d4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e69d4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69d4-131">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="e69d4-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="e69d4-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="e69d4-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="e69d4-133">**coclase**</span><span class="sxs-lookup"><span data-stu-id="e69d4-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="e69d4-134">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="e69d4-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e69d4-135">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="e69d4-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e69d4-136">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="e69d4-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="e69d4-137">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e69d4-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e69d4-138">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e69d4-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 