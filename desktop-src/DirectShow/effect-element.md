---
description: El elemento effect define un objeto de efecto de audio o vídeo. Un efecto se aplica a una sola secuencia (por ejemplo, una composición, una pista o un origen).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: elemento effect (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908663"
---
# <a name="effect-element"></a><span data-ttu-id="07c99-104">elemento effect</span><span class="sxs-lookup"><span data-stu-id="07c99-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="07c99-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="07c99-105">\[Deprecated.</span></span> <span data-ttu-id="07c99-106">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07c99-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07c99-107">El `effect` elemento define un objeto de efecto de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="07c99-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="07c99-108">Un efecto se aplica a una sola secuencia (por ejemplo, una composición, una pista o un origen).</span><span class="sxs-lookup"><span data-stu-id="07c99-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="07c99-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="07c99-109">Attributes</span></span>

<span data-ttu-id="07c99-110">[**clsid,**](clsid-attribute.md) [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="07c99-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="07c99-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="07c99-111">Parent/Child Information</span></span>



| <span data-ttu-id="07c99-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="07c99-112">Label</span></span> | <span data-ttu-id="07c99-113">Value</span><span class="sxs-lookup"><span data-stu-id="07c99-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c99-114">Parent</span><span class="sxs-lookup"><span data-stu-id="07c99-114">Parent</span></span>   | <span data-ttu-id="07c99-115">[**compuesto,**](composite-element.md) [**grupo,**](group-element.md) [**clip,**](clip-element.md) [**pista**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="07c99-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="07c99-116">Children</span><span class="sxs-lookup"><span data-stu-id="07c99-116">Children</span></span> | [<span data-ttu-id="07c99-117">**param**</span><span class="sxs-lookup"><span data-stu-id="07c99-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="07c99-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07c99-118">Remarks</span></span>

<span data-ttu-id="07c99-119">El **atributo clsid** especifica el subobjeto que crea el efecto.</span><span class="sxs-lookup"><span data-stu-id="07c99-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="07c99-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="07c99-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="07c99-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c99-121">Requirements</span></span>



| <span data-ttu-id="07c99-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c99-122">Requirement</span></span> | <span data-ttu-id="07c99-123">Value</span><span class="sxs-lookup"><span data-stu-id="07c99-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c99-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07c99-124">Header</span></span><br/> | <dl> <span data-ttu-id="07c99-125"><dt>Gdipluseffects.h</dt></span><span class="sxs-lookup"><span data-stu-id="07c99-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c99-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="07c99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c99-127">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="07c99-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




