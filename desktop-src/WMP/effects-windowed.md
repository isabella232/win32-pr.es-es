---
title: EFFECTs. windowed
description: El atributo windowed especifica o recupera un valor que indica si la visualización se va a mostrar o no en ventanas, es decir, si todo el rectángulo del control será visible en todo momento o si se puede recortar.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFECTOS. ventanas de Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700343"
---
# <a name="effectswindowed"></a><span data-ttu-id="78ef2-104">EFFECTs. windowed</span><span class="sxs-lookup"><span data-stu-id="78ef2-104">EFFECTS.windowed</span></span>

<span data-ttu-id="78ef2-105">El atributo **windowed** especifica o recupera un valor que indica si la visualización se va a mostrar o no en ventanas, es decir, si todo el rectángulo del control será visible en todo momento o si se puede recortar.</span><span class="sxs-lookup"><span data-stu-id="78ef2-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="78ef2-106">Este atributo solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="78ef2-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="78ef2-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="78ef2-107">Possible Values</span></span>

<span data-ttu-id="78ef2-108">Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura después.</span><span class="sxs-lookup"><span data-stu-id="78ef2-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="78ef2-109">Value</span><span class="sxs-lookup"><span data-stu-id="78ef2-109">Value</span></span> | <span data-ttu-id="78ef2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78ef2-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="78ef2-111">true</span><span class="sxs-lookup"><span data-stu-id="78ef2-111">true</span></span>  | <span data-ttu-id="78ef2-112">El control se mostrará en la ventana.</span><span class="sxs-lookup"><span data-stu-id="78ef2-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="78ef2-113">false</span><span class="sxs-lookup"><span data-stu-id="78ef2-113">false</span></span> | <span data-ttu-id="78ef2-114">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="78ef2-114">Default.</span></span> <span data-ttu-id="78ef2-115">El control no tendrá ventanas.</span><span class="sxs-lookup"><span data-stu-id="78ef2-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="78ef2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78ef2-116">Remarks</span></span>

<span data-ttu-id="78ef2-117">Si se desea una ventana de visualización no rectangular, o si una imagen incluye alguna parte de la ventana, este atributo debe establecerse en false.</span><span class="sxs-lookup"><span data-stu-id="78ef2-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="78ef2-118">Esto sacrifica algún rendimiento para realizar el recorte necesario.</span><span class="sxs-lookup"><span data-stu-id="78ef2-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="78ef2-119">Si **windowed** está establecido en true, se omite cualquier imagen que abarque la ventana de visualización y la ventana de visualización tiene el orden z de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="78ef2-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="78ef2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78ef2-120">Requirements</span></span>



| <span data-ttu-id="78ef2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ef2-121">Requirement</span></span> | <span data-ttu-id="78ef2-122">Value</span><span class="sxs-lookup"><span data-stu-id="78ef2-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="78ef2-123">Versión</span><span class="sxs-lookup"><span data-stu-id="78ef2-123">Version</span></span><br/> | <span data-ttu-id="78ef2-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="78ef2-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78ef2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="78ef2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ef2-126">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="78ef2-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





