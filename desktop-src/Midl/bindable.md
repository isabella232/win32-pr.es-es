---
title: bindable (atributo)
description: El atributo \ Bindable \ indica que la propiedad admite el enlace de datos.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- MIDL del atributo enlazable
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685698"
---
# <a name="bindable-attribute"></a><span data-ttu-id="12252-104">bindable (atributo)</span><span class="sxs-lookup"><span data-stu-id="12252-104">bindable attribute</span></span>

<span data-ttu-id="12252-105">El atributo **\[ Bindable \]** indica que la propiedad admite el enlace de datos.</span><span class="sxs-lookup"><span data-stu-id="12252-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="12252-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12252-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="12252-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-108">Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="12252-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="12252-109">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="12252-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="12252-110">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="12252-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-111">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="12252-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="12252-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="12252-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-113">Especifica cero o más atributos que se aplican al prototipo de función para una propiedad o un método en una [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="12252-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="12252-114">Los atributos siguientes son válidos: [**\[ \] HelpString**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ PROPPUT \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)y [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="12252-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="12252-115">Si se especifica **vararg** , el último parámetro debe ser una matriz segura de tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="12252-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="12252-116">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="12252-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="12252-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="12252-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-118">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="12252-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="12252-119">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="12252-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-120">Especifica el nombre de la función a la que se aplicará el atributo **\[ enlazable \]** .</span><span class="sxs-lookup"><span data-stu-id="12252-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="12252-121">*params*</span><span class="sxs-lookup"><span data-stu-id="12252-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="12252-122">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="12252-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12252-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12252-123">Remarks</span></span>

<span data-ttu-id="12252-124">Al admitir el enlace de datos, el atributo **\[ enlazable \]** permite al cliente recibir una notificación cada vez que una propiedad ha cambiado de valor.</span><span class="sxs-lookup"><span data-stu-id="12252-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="12252-125">(Si desea que el cliente reciba notificaciones de cambios inminentes en una propiedad, use el atributo [**\[ requestedit \]**](requestedit.md) ).</span><span class="sxs-lookup"><span data-stu-id="12252-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="12252-126">Dado que el atributo **\[ enlazable \]** hace referencia a la propiedad como un todo, se debe especificar dondequiera que se defina la propiedad.</span><span class="sxs-lookup"><span data-stu-id="12252-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="12252-127">Por lo tanto, debe especificar el atributo en la función de acceso a propiedades y en la función de configuración de propiedades.</span><span class="sxs-lookup"><span data-stu-id="12252-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="12252-128">Marcas</span><span class="sxs-lookup"><span data-stu-id="12252-128">Flags</span></span>

<span data-ttu-id="12252-129">FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE</span><span class="sxs-lookup"><span data-stu-id="12252-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="12252-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="12252-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="12252-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="12252-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12252-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="12252-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="12252-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="12252-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="12252-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="12252-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="12252-135">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="12252-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="12252-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="12252-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="12252-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="12252-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="12252-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="12252-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="12252-139">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="12252-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="12252-140">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="12252-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="12252-141">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="12252-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="12252-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="12252-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="12252-143">**PROPPUT**</span><span class="sxs-lookup"><span data-stu-id="12252-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="12252-144">**PROPPUTREF**</span><span class="sxs-lookup"><span data-stu-id="12252-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="12252-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="12252-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="12252-146">**string**</span><span class="sxs-lookup"><span data-stu-id="12252-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="12252-147">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="12252-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="12252-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="12252-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 