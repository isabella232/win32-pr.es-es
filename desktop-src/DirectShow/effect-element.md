---
description: El elemento Effect define un objeto de audio o de efecto de vídeo. Se aplica un efecto a un flujo único (como una composición, pista u origen).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653879"
---
# <a name="effect-element"></a><span data-ttu-id="fc310-104">Elemento Effect</span><span class="sxs-lookup"><span data-stu-id="fc310-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="fc310-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fc310-105">\[Deprecated.</span></span> <span data-ttu-id="fc310-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc310-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fc310-107">El `effect` elemento define un objeto de audio o de efecto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc310-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="fc310-108">Se aplica un efecto a un flujo único (como una composición, pista u origen).</span><span class="sxs-lookup"><span data-stu-id="fc310-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="fc310-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc310-109">Attributes</span></span>

<span data-ttu-id="fc310-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="fc310-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="fc310-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="fc310-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc310-112">Parent</span><span class="sxs-lookup"><span data-stu-id="fc310-112">Parent</span></span>   | <span data-ttu-id="fc310-113">[**compuesto**](composite-element.md), [**agrupar**](group-element.md), [**recortar**](clip-element.md), [**hacer seguimiento**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="fc310-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="fc310-114">Children</span><span class="sxs-lookup"><span data-stu-id="fc310-114">Children</span></span> | [<span data-ttu-id="fc310-115">**param**</span><span class="sxs-lookup"><span data-stu-id="fc310-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="fc310-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc310-116">Remarks</span></span>

<span data-ttu-id="fc310-117">El atributo **CLSID** especifica el subobjeto que crea el efecto.</span><span class="sxs-lookup"><span data-stu-id="fc310-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="fc310-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fc310-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="fc310-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc310-119">Requirements</span></span>



| <span data-ttu-id="fc310-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc310-120">Requirement</span></span> | <span data-ttu-id="fc310-121">Value</span><span class="sxs-lookup"><span data-stu-id="fc310-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc310-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc310-122">Header</span></span><br/> | <dl> <span data-ttu-id="fc310-123"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc310-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc310-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc310-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc310-125">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="fc310-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




