---
title: SEEKSLIDER
description: Este es un control deslizante predefinido con los siguientes valores predeterminados. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649614"
---
# <a name="seekslider"></a><span data-ttu-id="781c1-105">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="781c1-105">SEEKSLIDER</span></span>

<span data-ttu-id="781c1-106">Este es un **control deslizante** predefinido con los siguientes valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="781c1-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="781c1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="781c1-107">Remarks</span></span>

<span data-ttu-id="781c1-108">Esto crea un control **deslizante** que busca el archivo multimedia en cualquier posición.</span><span class="sxs-lookup"><span data-stu-id="781c1-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="781c1-109">La información sobre herramientas está localizada.</span><span class="sxs-lookup"><span data-stu-id="781c1-109">The ToolTips are localized.</span></span> <span data-ttu-id="781c1-110">Todas las propiedades de este **control deslizante** se pueden invalidar si se especifican de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="781c1-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="781c1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="781c1-111">Requirements</span></span>



| <span data-ttu-id="781c1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="781c1-112">Requirement</span></span> | <span data-ttu-id="781c1-113">Value</span><span class="sxs-lookup"><span data-stu-id="781c1-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="781c1-114">Versión</span><span class="sxs-lookup"><span data-stu-id="781c1-114">Version</span></span><br/> | <span data-ttu-id="781c1-115">Windows Media Player 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="781c1-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="781c1-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="781c1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781c1-117">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="781c1-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





