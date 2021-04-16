---
title: nonextensible (atributo)
description: El atributo \ nonextensible (\ especifica que la implementación de IDispatch solo incluye las propiedades y los métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nonextensible ((atributo) MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651352"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="84352-104">nonextensible (atributo)</span><span class="sxs-lookup"><span data-stu-id="84352-104">nonextensible attribute</span></span>

<span data-ttu-id="84352-105">El atributo **\[ \] nonextensible (** especifica que la implementación de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) solo incluye las propiedades y los métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="84352-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="84352-106">(De forma predeterminada, la automatización presupone que las interfaces pueden agregar miembros en tiempo de ejecución; es decir, se supone que son extensibles).</span><span class="sxs-lookup"><span data-stu-id="84352-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="84352-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84352-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84352-108">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="84352-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="84352-109">Especifica un número de identificación único universal para la [**interfaz**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="84352-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="84352-110">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="84352-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="84352-111">Especifica una lista de cero o más atributos de la interfaz de MIDL.</span><span class="sxs-lookup"><span data-stu-id="84352-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="84352-112">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="84352-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="84352-113">Especifica el nombre de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="84352-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="84352-114">*definición de interfaz*</span><span class="sxs-lookup"><span data-stu-id="84352-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="84352-115">Especifica instrucciones IDL que forman la definición de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="84352-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84352-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84352-116">Remarks</span></span>

<span data-ttu-id="84352-117">Puede aplicar el atributo **\[ nonextensible ( \]** a una interfaz o dispinterface.</span><span class="sxs-lookup"><span data-stu-id="84352-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="84352-118">Sin embargo, una interfaz también debe tener los **\[** atributos [**dual**](dual.md) **\]** y **\[** [**oleautomation**](oleautomation.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="84352-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="84352-119">Marcas</span><span class="sxs-lookup"><span data-stu-id="84352-119">Flags</span></span>

<span data-ttu-id="84352-120">TYPEFLAG \_ FNONEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="84352-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="84352-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84352-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="84352-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="84352-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84352-123">Contenido de una biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84352-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="84352-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="84352-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="84352-125">**BI**</span><span class="sxs-lookup"><span data-stu-id="84352-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="84352-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="84352-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="84352-127">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="84352-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="84352-128">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="84352-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="84352-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="84352-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="84352-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="84352-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 