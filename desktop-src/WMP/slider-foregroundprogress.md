---
title: SLIDEr. foregroundProgress
description: El atributo foregroundProgress especifica o recupera la posición actual de la barra de progreso del primer plano como un porcentaje del área del control deslizante.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- CONTROL SLIDEr. foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661000"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="353d3-104">SLIDEr. foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="353d3-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="353d3-105">El atributo **foregroundProgress** especifica o recupera la posición actual de la barra de progreso del primer plano como un porcentaje del área del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="353d3-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="353d3-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="353d3-106">Possible Values</span></span>

<span data-ttu-id="353d3-107">Este atributo es un **número** de lectura/escritura (**float**) que va de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="353d3-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="353d3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353d3-108">Remarks</span></span>

<span data-ttu-id="353d3-109">Este atributo se usa principalmente para realizar el seguimiento del progreso de la descarga de un archivo multimedia mientras realiza un seguimiento simultáneo de la posición de reproducción actual del archivo mediante el atributo de **valor** .</span><span class="sxs-lookup"><span data-stu-id="353d3-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="353d3-110">La posición del control deslizante está restringida al área del progreso en primer plano.</span><span class="sxs-lookup"><span data-stu-id="353d3-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="353d3-111">Esto permite que la búsqueda interactiva tenga lugar solo dentro de la parte disponible de un archivo de descarga.</span><span class="sxs-lookup"><span data-stu-id="353d3-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="353d3-112">Para usar esta funcionalidad, el atributo **useForegroundProgress** debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="353d3-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="353d3-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="353d3-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="353d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="353d3-114">Requirements</span></span>



| <span data-ttu-id="353d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="353d3-115">Requirement</span></span> | <span data-ttu-id="353d3-116">Value</span><span class="sxs-lookup"><span data-stu-id="353d3-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="353d3-117">Versión</span><span class="sxs-lookup"><span data-stu-id="353d3-117">Version</span></span><br/> | <span data-ttu-id="353d3-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="353d3-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="353d3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="353d3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353d3-120">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="353d3-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="353d3-121">**SLIDEr. min**</span><span class="sxs-lookup"><span data-stu-id="353d3-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="353d3-122">**Control deslizante. Max**</span><span class="sxs-lookup"><span data-stu-id="353d3-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="353d3-123">**SLIDEr. useForegroundProgress**</span><span class="sxs-lookup"><span data-stu-id="353d3-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="353d3-124">**Control deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="353d3-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





