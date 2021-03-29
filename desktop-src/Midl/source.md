---
title: source (atributo)
description: El atributo \ Source \ indica que un miembro de una coclase, propiedad o método es un origen de eventos. Para un miembro de una coclase, este atributo significa que se llama al miembro en lugar de implementarlo.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- atributo de origen MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995130"
---
# <a name="source-attribute"></a><span data-ttu-id="7471b-105">source (atributo)</span><span class="sxs-lookup"><span data-stu-id="7471b-105">source attribute</span></span>

<span data-ttu-id="7471b-106">El atributo de **\[ origen \]** indica que un miembro de una [**coclase**](coclass.md), propiedad o método es un origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="7471b-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="7471b-107">Para un miembro de una **coclase**, este atributo significa que se llama al miembro en lugar de implementarlo.</span><span class="sxs-lookup"><span data-stu-id="7471b-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="7471b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7471b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7471b-109">*coclase: atributos*</span><span class="sxs-lookup"><span data-stu-id="7471b-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-110">Cero o más atributos que se aplicarán a la [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="7471b-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="7471b-111">*nombre de coclase*</span><span class="sxs-lookup"><span data-stu-id="7471b-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-112">Identificador de nombre de la [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="7471b-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="7471b-113">*opcional: atributos*</span><span class="sxs-lookup"><span data-stu-id="7471b-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-114">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7471b-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7471b-115">*tipo de instrucción*</span><span class="sxs-lookup"><span data-stu-id="7471b-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-116">Puede ser [**interface**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7471b-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7471b-117">*nombre de instrucción*</span><span class="sxs-lookup"><span data-stu-id="7471b-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-118">Nombre de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7471b-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7471b-119">*tipo de objeto*</span><span class="sxs-lookup"><span data-stu-id="7471b-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-120">Tipo del objeto que devuelve el método.</span><span class="sxs-lookup"><span data-stu-id="7471b-120">The type of the object that the method returns.</span></span> <span data-ttu-id="7471b-121">Este objeto es un origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="7471b-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="7471b-122">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="7471b-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-123">Nombre de un método en una [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7471b-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7471b-124">*opcional-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="7471b-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7471b-125">Cero o más parámetros de método.</span><span class="sxs-lookup"><span data-stu-id="7471b-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7471b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7471b-126">Remarks</span></span>

<span data-ttu-id="7471b-127">En una propiedad o método, el atributo de **\[ origen \]** indica que el miembro devuelve un objeto o una variante que es un origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="7471b-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="7471b-128">El objeto implementa **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="7471b-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="7471b-129">Marcas</span><span class="sxs-lookup"><span data-stu-id="7471b-129">Flags</span></span>

<span data-ttu-id="7471b-130">IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ source, FUNCFLAG \_ source</span><span class="sxs-lookup"><span data-stu-id="7471b-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="7471b-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7471b-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="7471b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7471b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7471b-133">**coclase**</span><span class="sxs-lookup"><span data-stu-id="7471b-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="7471b-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="7471b-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7471b-135">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="7471b-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7471b-136">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="7471b-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7471b-137">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="7471b-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7471b-138">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="7471b-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7471b-139">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7471b-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 