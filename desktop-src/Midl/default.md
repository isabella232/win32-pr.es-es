---
title: atributo predeterminado
description: El atributo \ default \ indica que la interfaz o la dispinterface, definidas dentro de una coclase, representa la interfaz de programación predeterminada. Este atributo está pensado para que lo usen los lenguajes de macros.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- valor predeterminado del atributo MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487586"
---
# <a name="default-attribute"></a><span data-ttu-id="98e17-105">atributo predeterminado</span><span class="sxs-lookup"><span data-stu-id="98e17-105">default attribute</span></span>

<span data-ttu-id="98e17-106">El atributo **\[ \] default** indica que la [**interfaz**](interface.md) o la [**dispinterface**](dispinterface.md), definidas dentro de una [**coclase**](coclass.md), representa la interfaz de programación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98e17-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="98e17-107">Este atributo está pensado para que lo usen los lenguajes de macros.</span><span class="sxs-lookup"><span data-stu-id="98e17-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="98e17-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98e17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e17-109">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="98e17-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="98e17-110">Especifica un número de identificación único universal para la [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="98e17-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e17-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="98e17-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="98e17-112">Especifica atributos de [**coclase**](coclass.md) adicionales.</span><span class="sxs-lookup"><span data-stu-id="98e17-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="98e17-113">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="98e17-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="98e17-114">*nombre de coclase*</span><span class="sxs-lookup"><span data-stu-id="98e17-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="98e17-115">Especifica el nombre por el que otros componentes de software pueden hacer referencia a esta [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="98e17-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e17-116">*Optional-interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="98e17-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="98e17-117">El **\[** atributo de [**origen**](source.md) **\]** , que especifica que una interfaz o dispinterface es saliente, es el único otro atributo que se puede utilizar aquí.</span><span class="sxs-lookup"><span data-stu-id="98e17-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="98e17-118">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="98e17-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="98e17-119">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="98e17-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98e17-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98e17-120">Remarks</span></span>

<span data-ttu-id="98e17-121">Una [**coclase**](coclass.md) puede tener como máximo dos miembros **\[ predeterminados \]** .</span><span class="sxs-lookup"><span data-stu-id="98e17-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="98e17-122">Uno representa la interfaz de salida (origen) o la dispinterface, y el otro representa la interfaz (receptor) entrante o dispinterface.</span><span class="sxs-lookup"><span data-stu-id="98e17-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="98e17-123">Si no se especifica el atributo **\[ default \]** para ningún miembro de la **coclase** o **cotype**, los primeros miembros salientes y entrantes que no tienen el **\[** atributo [**Restricted**](restricted.md) **\]** se tratan como valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="98e17-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="98e17-124">Marcas</span><span class="sxs-lookup"><span data-stu-id="98e17-124">Flags</span></span>

<span data-ttu-id="98e17-125">IMPLTYPEFLAG \_ FDEFAULT</span><span class="sxs-lookup"><span data-stu-id="98e17-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="98e17-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="98e17-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="98e17-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="98e17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e17-128">**coclase**</span><span class="sxs-lookup"><span data-stu-id="98e17-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="98e17-129">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="98e17-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="98e17-130">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="98e17-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="98e17-131">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="98e17-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="98e17-132">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="98e17-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="98e17-133">**Restrict**</span><span class="sxs-lookup"><span data-stu-id="98e17-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="98e17-134">**fuentes**</span><span class="sxs-lookup"><span data-stu-id="98e17-134">**source**</span></span>](source.md)
</dt> </dl>

 

 