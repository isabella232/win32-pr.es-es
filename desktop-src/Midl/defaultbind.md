---
title: defaultbind (atributo)
description: El atributo \ defaultbind \ indica la única propiedad enlazable que mejor representa el objeto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- defaultbind (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077725"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="71d9d-104">defaultbind (atributo)</span><span class="sxs-lookup"><span data-stu-id="71d9d-104">defaultbind attribute</span></span>

<span data-ttu-id="71d9d-105">El atributo **\[ defaultbind \]** indica la única propiedad enlazable que representa mejor el objeto.</span><span class="sxs-lookup"><span data-stu-id="71d9d-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="71d9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71d9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d9d-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="71d9d-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-108">Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="71d9d-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="71d9d-109">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="71d9d-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="71d9d-110">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="71d9d-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-111">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="71d9d-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="71d9d-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="71d9d-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-113">Especifica una lista de uno o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="71d9d-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="71d9d-114">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="71d9d-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="71d9d-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="71d9d-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-116">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="71d9d-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="71d9d-117">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="71d9d-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-118">Especifica el nombre de la función a la que se aplicará el atributo **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="71d9d-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="71d9d-119">*params*</span><span class="sxs-lookup"><span data-stu-id="71d9d-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="71d9d-120">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="71d9d-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71d9d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71d9d-121">Remarks</span></span>

<span data-ttu-id="71d9d-122">Las propiedades que tienen el atributo **\[ defaultbind \]** también deben tener el **\[** atributo [**enlazable**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="71d9d-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="71d9d-123">Solo una propiedad de una interfaz o dispinterface puede tener el atributo **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="71d9d-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="71d9d-124">Este atributo lo usan los contenedores que tienen un modelo de usuario que implica un enlace a un objeto en lugar de enlazar a una propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="71d9d-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="71d9d-125">Un objeto puede admitir el enlace de datos pero no tiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="71d9d-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="71d9d-126">Marcas</span><span class="sxs-lookup"><span data-stu-id="71d9d-126">Flags</span></span>

<span data-ttu-id="71d9d-127">FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND</span><span class="sxs-lookup"><span data-stu-id="71d9d-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="71d9d-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71d9d-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="71d9d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="71d9d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d9d-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="71d9d-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="71d9d-131">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="71d9d-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="71d9d-132">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="71d9d-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="71d9d-133">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="71d9d-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="71d9d-134">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="71d9d-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 