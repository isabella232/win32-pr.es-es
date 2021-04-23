---
description: El elemento transition define un objeto de transición. Una transición es una transformación de dos entradas que da como resultado una transición de una secuencia (como una compuesta o una pista) a otra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: elemento transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910043"
---
# <a name="transition-element"></a><span data-ttu-id="86c9f-104">elemento transition</span><span class="sxs-lookup"><span data-stu-id="86c9f-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="86c9f-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="86c9f-105">\[Deprecated.</span></span> <span data-ttu-id="86c9f-106">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86c9f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="86c9f-107">El `transition` elemento define un objeto de transición.</span><span class="sxs-lookup"><span data-stu-id="86c9f-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="86c9f-108">Una transición es una transformación de dos entradas que da como resultado una transición de una secuencia (como una compuesta o una pista) a otra.</span><span class="sxs-lookup"><span data-stu-id="86c9f-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="86c9f-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="86c9f-109">Attributes</span></span>

<span data-ttu-id="86c9f-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="86c9f-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="86c9f-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="86c9f-111">Parent/Child Information</span></span>



| <span data-ttu-id="86c9f-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="86c9f-112">Label</span></span> | <span data-ttu-id="86c9f-113">Value</span><span class="sxs-lookup"><span data-stu-id="86c9f-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="86c9f-114">Parent</span><span class="sxs-lookup"><span data-stu-id="86c9f-114">Parent</span></span>   | <span data-ttu-id="86c9f-115">[**compuesto,**](composite-element.md) [ **pista**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="86c9f-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="86c9f-116">Children</span><span class="sxs-lookup"><span data-stu-id="86c9f-116">Children</span></span> | [<span data-ttu-id="86c9f-117">**param**</span><span class="sxs-lookup"><span data-stu-id="86c9f-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="86c9f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86c9f-118">Remarks</span></span>

<span data-ttu-id="86c9f-119">El **atributo clsid** especifica el subobjeto que crea la transición.</span><span class="sxs-lookup"><span data-stu-id="86c9f-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="86c9f-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86c9f-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="86c9f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="86c9f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c9f-122">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="86c9f-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



