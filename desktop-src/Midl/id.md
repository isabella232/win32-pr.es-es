---
title: Atributo id
description: El atributo \ ID \ especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- identificador del atributo MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420572"
---
# <a name="id-attribute"></a><span data-ttu-id="f1c3d-104">Atributo id</span><span class="sxs-lookup"><span data-stu-id="f1c3d-104">id attribute</span></span>

<span data-ttu-id="f1c3d-105">El atributo **\[ ID \]** especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).</span><span class="sxs-lookup"><span data-stu-id="f1c3d-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="f1c3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1c3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c3d-107">*identificador: número*</span><span class="sxs-lookup"><span data-stu-id="f1c3d-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c3d-108">DISPID para la función.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3d-109">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f1c3d-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c3d-110">Especifica una lista de cero o más atributos de la interfaz de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3d-111">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="f1c3d-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c3d-112">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3d-113">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="f1c3d-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c3d-114">Especifica el nombre de la función en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3d-115">*opcional-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="f1c3d-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c3d-116">Cero o más parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1c3d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1c3d-117">Remarks</span></span>

<span data-ttu-id="f1c3d-118">Utilice el atributo **\[ \] ID** cuando desee asignar un DISPID estándar (como el \_ valor de DISPID, el DISPID NEWENUM, \_ etc.) a un método o propiedad, o al implementar su propio **IDispatch:: Invoke** en lugar de delegar en **DispInvoke** / **ITypeInfo:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="f1c3d-119">Si no utiliza el atributo **\[ ID \]** en una interfaz, el compilador MIDL le asignará un DispId.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="f1c3d-120">Sin embargo, cuando se especifica una dispinterface mediante propiedades y métodos, se debe especificar un DISPID para cada propiedad y método.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="f1c3d-121">El *identificador-NUM* es un valor entero positivo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="f1c3d-122">Los identificadores negativos se reservan para su uso con la automatización.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="f1c3d-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f1c3d-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="f1c3d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1c3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3d-125">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="f1c3d-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f1c3d-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="f1c3d-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="f1c3d-127">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="f1c3d-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f1c3d-128">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="f1c3d-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f1c3d-129">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="f1c3d-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 