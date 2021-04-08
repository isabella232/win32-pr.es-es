---
title: strict_context_handle atributo)
description: El atributo \ \_ \_ ACF de identificador de contexto \ STRICT establece restricciones en los identificadores de contexto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995129"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="a7fc4-104">atributo de identificador de \_ contexto estricto \_</span><span class="sxs-lookup"><span data-stu-id="a7fc4-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="a7fc4-105">El atributo ACF de **\[ \_ \_ identificador \] de contexto estricto** establece restricciones en los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="a7fc4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7fc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fc4-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="a7fc4-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7fc4-108">Otros atributos ACF que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a7fc4-109">Los atributos válidos incluyen el [**\_ identificador automático**](auto-handle.md), el [**\_ identificador implícito**](implicit-handle.md), el [**\_ identificador explícito**](explicit-handle.md)y [**Optimize**](optimize.md), [**code**](code.md)o [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="a7fc4-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="a7fc4-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a7fc4-111">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="a7fc4-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7fc4-112">Nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a7fc4-113">*instrucciones de interface-Definition*</span><span class="sxs-lookup"><span data-stu-id="a7fc4-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="a7fc4-114">Una o más instrucciones de MIDL que definen los elementos de la [**interfaz**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="a7fc4-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7fc4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7fc4-115">Remarks</span></span>

<span data-ttu-id="a7fc4-116">Normalmente, cuando una llamada a un método de interfaz genera un identificador de contexto, ese identificador está disponible libremente para cualquier otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="a7fc4-117">Cuando use el atributo de **\[ \_ \_ identificador \] de contexto STRICT** , garantizará que los métodos de esa interfaz solo aceptarán los identificadores de contexto creados por un método de la misma interfaz.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="a7fc4-118">Las interfaces compiladas sin un **\[ \_ \_ identificador \] de contexto estricto** no pueden aceptar identificadores de contexto creados en interfaces compiladas con un **\[ \_ \_ \] identificador de contexto estricto**.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7fc4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7fc4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fc4-120">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="a7fc4-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-121">**codifica**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-122">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="a7fc4-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="a7fc4-123">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-124">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-125">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-126">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-127">**nocode**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-128">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-129">escribir \_ el \_ identificador de contexto STRICT \_</span><span class="sxs-lookup"><span data-stu-id="a7fc4-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 