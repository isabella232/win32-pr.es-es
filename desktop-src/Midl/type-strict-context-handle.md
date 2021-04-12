---
title: type_strict_context_handle atributo)
description: Use el controlador de \_ contexto \ tipo STRICT \_ \_ en un archivo ACF para establecer restricciones en los identificadores de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487558"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="3f39b-104">escribir \_ \_ atributo de identificador de contexto STRICT \_</span><span class="sxs-lookup"><span data-stu-id="3f39b-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="3f39b-105">Use el **\[ tipo \_ de \_ \_ identificador \] de contexto STRICT** en un archivo ACF para establecer restricciones en los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="3f39b-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="3f39b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f39b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f39b-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="3f39b-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3f39b-108">Otros atributos ACF que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="3f39b-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="3f39b-109">Los atributos válidos incluyen el [**\_ identificador automático**](auto-handle.md), el [**\_ identificador implícito**](implicit-handle.md), el [**\_ identificador explícito**](explicit-handle.md)y [**Optimize**](optimize.md), [**code**](code.md)o [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="3f39b-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="3f39b-110">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="3f39b-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3f39b-111">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="3f39b-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3f39b-112">Nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3f39b-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3f39b-113">*instrucciones de interface-Definition*</span><span class="sxs-lookup"><span data-stu-id="3f39b-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="3f39b-114">Una o más instrucciones de MIDL que definen los elementos de la [**interfaz**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="3f39b-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f39b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f39b-115">Remarks</span></span>

<span data-ttu-id="3f39b-116">Para usar este atributo, la marca-Target se debe establecer en NT60 (o superior) cuando se ejecuta midl.exe.</span><span class="sxs-lookup"><span data-stu-id="3f39b-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="3f39b-117">\[\_el tipo \_ \_ de identificador de contexto STRICT \] es un supraconjunto funcional de \[ identificador de contexto estricto \_ \_ \] .</span><span class="sxs-lookup"><span data-stu-id="3f39b-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="3f39b-118">En el identificador de \[ \_ contexto estricto \_ \] , el identificador de tipo del identificador es siempre 0; en \[ \_ el identificador de contexto de tipo STRICT \_ \_ \] , el compilador MIDL asigna un identificador de tipo único.</span><span class="sxs-lookup"><span data-stu-id="3f39b-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="3f39b-119">Se recomienda usar un \[ \_ \_ identificador de contexto estricto \_ \] en lugar de \[ un \_ identificador de contexto estricto \_ \] .</span><span class="sxs-lookup"><span data-stu-id="3f39b-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="3f39b-120">Los identificadores de contexto no se asocian a un tipo específico de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f39b-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="3f39b-121">Cuando se usan varios tipos de identificadores de contexto en el mismo proceso, es posible que un cliente malintencionado pase un identificador de contexto en lugar de otro para producir resultados no deseados.</span><span class="sxs-lookup"><span data-stu-id="3f39b-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="3f39b-122">El uso del \[ \_ identificador de contexto STRICT de tipo \_ \_ \] permite a las aplicaciones aplicar la coherencia del tipo de identificador de contexto y evitar el uso del tipo de identificador de contexto no coincidente.</span><span class="sxs-lookup"><span data-stu-id="3f39b-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="3f39b-123">Un identificador de contexto con el atributo de \[ \_ identificador de \_ contexto STRICT \_ \] no se puede atribuir con un \[ identificador de contexto estricto \_ \_ \] .</span><span class="sxs-lookup"><span data-stu-id="3f39b-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="3f39b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f39b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f39b-125">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="3f39b-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="3f39b-126">**codifica**</span><span class="sxs-lookup"><span data-stu-id="3f39b-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="3f39b-127">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="3f39b-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="3f39b-128">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="3f39b-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="3f39b-129">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="3f39b-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="3f39b-130">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="3f39b-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="3f39b-131">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="3f39b-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="3f39b-132">**nocode**</span><span class="sxs-lookup"><span data-stu-id="3f39b-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="3f39b-133">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="3f39b-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="3f39b-134">\_identificador de contexto estricto \_</span><span class="sxs-lookup"><span data-stu-id="3f39b-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 