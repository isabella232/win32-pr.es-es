---
title: immediatebind (atributo)
description: El atributo \ immediatebind \ indica que se notificará inmediatamente a la base de datos todos los cambios en una propiedad de un objeto enlazado a datos.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind (atributo) MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270839"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="4fa16-104">immediatebind (atributo)</span><span class="sxs-lookup"><span data-stu-id="4fa16-104">immediatebind attribute</span></span>

<span data-ttu-id="4fa16-105">El atributo **\[ immediatebind \]** indica que se notificará inmediatamente a la base de datos todos los cambios en una propiedad de un objeto enlazado a datos.</span><span class="sxs-lookup"><span data-stu-id="4fa16-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="4fa16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fa16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa16-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="4fa16-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-108">Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="4fa16-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="4fa16-109">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="4fa16-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-110">Especifica el nombre de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="4fa16-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fa16-111">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4fa16-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-112">Cero o más atributos de función.</span><span class="sxs-lookup"><span data-stu-id="4fa16-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4fa16-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="4fa16-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-114">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="4fa16-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4fa16-115">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="4fa16-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-116">Especifica el nombre de la función en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="4fa16-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="4fa16-117">*params*</span><span class="sxs-lookup"><span data-stu-id="4fa16-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa16-118">Cero o más parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="4fa16-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fa16-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fa16-119">Remarks</span></span>

<span data-ttu-id="4fa16-120">El atributo **\[ immediatebind \]** permite a los controles diferenciar entre las propiedades que necesitan notificar a la base de datos todos los cambios y las que no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="4fa16-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="4fa16-121">Por ejemplo, cada cambio en un control CheckBox debe enviarse inmediatamente a la base de datos subyacente, incluso si el control no ha perdido el foco.</span><span class="sxs-lookup"><span data-stu-id="4fa16-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="4fa16-122">Sin embargo, para un control ListBox, se produce un cambio cada vez que se resalta una selección diferente.</span><span class="sxs-lookup"><span data-stu-id="4fa16-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="4fa16-123">Notificar a la base de datos un cambio antes de que el control pierda el foco sería ineficaz e innecesario.</span><span class="sxs-lookup"><span data-stu-id="4fa16-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="4fa16-124">El atributo **\[ immediatebind \]** permite especificar, estableciendo el bit immediatebind, propiedades individuales en un formulario cuyos cambios se deben notificar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4fa16-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="4fa16-125">Las propiedades que tienen el atributo **\[ immediatebind \]** también deben tener el **\[** atributo [**enlazable**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fa16-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="4fa16-126">Marcas</span><span class="sxs-lookup"><span data-stu-id="4fa16-126">Flags</span></span>

<span data-ttu-id="4fa16-127">FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND</span><span class="sxs-lookup"><span data-stu-id="4fa16-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="4fa16-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4fa16-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="4fa16-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fa16-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa16-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="4fa16-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="4fa16-131">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="4fa16-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="4fa16-132">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="4fa16-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4fa16-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="4fa16-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4fa16-134">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="4fa16-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4fa16-135">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="4fa16-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4fa16-136">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="4fa16-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 