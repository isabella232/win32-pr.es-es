---
title: modificador/ms_union
description: El \_ modificador de/MS Union controla la alineación del NDR de las uniones no encapsuladas. Nota Este atributo se proporciona por compatibilidad con versiones anteriores.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union modificador MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904176"
---
# <a name="ms_union-switch"></a><span data-ttu-id="d8fbd-104">\_conmutador de Unión/MS</span><span class="sxs-lookup"><span data-stu-id="d8fbd-104">/ms\_union switch</span></span>

<span data-ttu-id="d8fbd-105">El modificador de **/MS \_ Union** controla la alineación del NDR de las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="d8fbd-106">Este atributo se proporciona por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="d8fbd-107">No se recomienda su uso en una nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="d8fbd-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="d8fbd-108">Switch Options</span></span>

<span data-ttu-id="d8fbd-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fbd-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8fbd-110">Remarks</span></span>

<span data-ttu-id="d8fbd-111">El compilador MIDL refleja el comportamiento del compilador de de OSF-DCE IDL para las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="d8fbd-112">Sin embargo, dado que las versiones anteriores del compilador de MIDL no lo hacían, el modificador **/MS \_ Union** proporciona compatibilidad con las interfaces creadas en versiones anteriores del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="d8fbd-113">La \_ característica MS Union se puede usar como un modificador de la línea de comandos (**/MS \_ Union**), un atributo de interfaz IDL o como un atributo de tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="d8fbd-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d8fbd-114">Examples</span></span>

<span data-ttu-id="d8fbd-115">**archivo de \_ Unión MIDL/ms. idl**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d8fbd-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8fbd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fbd-117">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="d8fbd-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d8fbd-118">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




