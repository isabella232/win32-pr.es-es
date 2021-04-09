---
title: displaybind (atributo)
description: El atributo \ displaybind \ indica una propiedad que se debe mostrar al usuario como enlazable.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- displaybind (atributo) MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790227"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="fd715-104">displaybind (atributo)</span><span class="sxs-lookup"><span data-stu-id="fd715-104">displaybind attribute</span></span>

<span data-ttu-id="fd715-105">El atributo **\[ displaybind \]** indica una propiedad que se debe mostrar al usuario como enlazable.</span><span class="sxs-lookup"><span data-stu-id="fd715-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="fd715-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd715-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="fd715-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-108">Especifica una lista opcional de atributos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="fd715-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="fd715-109">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="fd715-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-110">Nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="fd715-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="fd715-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="fd715-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-112">Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo de valor devuelto de función.</span><span class="sxs-lookup"><span data-stu-id="fd715-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="fd715-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="fd715-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-114">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="fd715-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="fd715-115">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="fd715-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-116">Especifica el nombre de la función a la que se aplicará el atributo **\[ displaybind \]** .</span><span class="sxs-lookup"><span data-stu-id="fd715-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="fd715-117">*params*</span><span class="sxs-lookup"><span data-stu-id="fd715-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fd715-118">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="fd715-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd715-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd715-119">Remarks</span></span>

<span data-ttu-id="fd715-120">Las propiedades que tienen el atributo **\[ displaybind \]** también deben tener el **\[** atributo [**enlazable**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fd715-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="fd715-121">Un objeto puede admitir el enlace de datos pero no tiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="fd715-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="fd715-122">Marcas</span><span class="sxs-lookup"><span data-stu-id="fd715-122">Flags</span></span>

<span data-ttu-id="fd715-123">FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND</span><span class="sxs-lookup"><span data-stu-id="fd715-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="fd715-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fd715-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="fd715-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd715-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd715-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="fd715-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="fd715-127">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="fd715-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="fd715-128">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="fd715-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fd715-129">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="fd715-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fd715-130">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="fd715-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 