---
title: control (atributo)
description: El atributo \ control \ identifica una coclase o biblioteca como control COM, de la que un sitio de contenedor derivará bibliotecas de tipos o clases de objetos de componente adicionales.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- MIDL (atributo de control)
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789867"
---
# <a name="control-attribute"></a><span data-ttu-id="5a55a-104">control (atributo)</span><span class="sxs-lookup"><span data-stu-id="5a55a-104">control attribute</span></span>

<span data-ttu-id="5a55a-105">El atributo **\[ control \]** identifica una [**coclase**](coclass.md) o [**biblioteca**](library.md) como un control com, desde el que un sitio contenedor derivará bibliotecas de tipos o clases de objetos de componente adicionales.</span><span class="sxs-lookup"><span data-stu-id="5a55a-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="5a55a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a55a-107">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="5a55a-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5a55a-108">Especifica cero o más atributos que se aplican a la instrucción [**Library**](library.md) o [**CoClass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="5a55a-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="5a55a-109">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="5a55a-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5a55a-110">*lib o coclassname*</span><span class="sxs-lookup"><span data-stu-id="5a55a-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="5a55a-111">Especifica el nombre de la [**biblioteca**](library.md) o [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="5a55a-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a55a-112">*Figura*</span><span class="sxs-lookup"><span data-stu-id="5a55a-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="5a55a-113">Instrucciones de MIDL que especifican los miembros de la [**biblioteca**](library.md) o [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="5a55a-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a55a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a55a-114">Remarks</span></span>

<span data-ttu-id="5a55a-115">Este atributo le permite marcar las bibliotecas de tipos que describen los controles para que no se muestren en exploradores de tipos destinados a objetos no visuales.</span><span class="sxs-lookup"><span data-stu-id="5a55a-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="5a55a-116">Marcas</span><span class="sxs-lookup"><span data-stu-id="5a55a-116">Flags</span></span>

<span data-ttu-id="5a55a-117">TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL</span><span class="sxs-lookup"><span data-stu-id="5a55a-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="5a55a-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5a55a-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="5a55a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a55a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a55a-120">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5a55a-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5a55a-121">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5a55a-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5a55a-122">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="5a55a-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="5a55a-123">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="5a55a-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="5a55a-124">**coclase**</span><span class="sxs-lookup"><span data-stu-id="5a55a-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="5a55a-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="5a55a-125">**library**</span></span>](library.md)
</dt> </dl>

 

 