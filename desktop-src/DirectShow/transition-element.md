---
description: El elemento Transition define un objeto Transition. Una transición es una transformación de dos entradas que da como resultado una transición de un flujo (como un compuesto o un seguimiento) a otra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento Transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667642"
---
# <a name="transition-element"></a><span data-ttu-id="82bc6-104">Elemento Transition</span><span class="sxs-lookup"><span data-stu-id="82bc6-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="82bc6-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="82bc6-105">\[Deprecated.</span></span> <span data-ttu-id="82bc6-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82bc6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82bc6-107">El `transition` elemento define un objeto de transición.</span><span class="sxs-lookup"><span data-stu-id="82bc6-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="82bc6-108">Una transición es una transformación de dos entradas que da como resultado una transición de un flujo (como un compuesto o un seguimiento) a otra.</span><span class="sxs-lookup"><span data-stu-id="82bc6-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="82bc6-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="82bc6-109">Attributes</span></span>

<span data-ttu-id="82bc6-110">[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="82bc6-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="82bc6-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="82bc6-111">Parent/Child Information</span></span>



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="82bc6-112">Parent</span><span class="sxs-lookup"><span data-stu-id="82bc6-112">Parent</span></span>   | <span data-ttu-id="82bc6-113">[**compuesto**](composite-element.md), [ **seguimiento**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="82bc6-113">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="82bc6-114">Children</span><span class="sxs-lookup"><span data-stu-id="82bc6-114">Children</span></span> | [<span data-ttu-id="82bc6-115">**param**</span><span class="sxs-lookup"><span data-stu-id="82bc6-115">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="82bc6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82bc6-116">Remarks</span></span>

<span data-ttu-id="82bc6-117">El atributo **CLSID** especifica el subobjeto que crea la transición.</span><span class="sxs-lookup"><span data-stu-id="82bc6-117">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="82bc6-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82bc6-118">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="82bc6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="82bc6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bc6-120">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="82bc6-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



