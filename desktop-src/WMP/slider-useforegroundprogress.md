---
title: SLIDEr. useForegroundProgress
description: El atributo useForegroundProgress especifica o recupera un valor que indica si se utilizará la barra de progreso en primer plano.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- CONTROL SLIDEr. useForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660289"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="6c9b9-104">SLIDEr. useForegroundProgress</span><span class="sxs-lookup"><span data-stu-id="6c9b9-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="6c9b9-105">El atributo **useForegroundProgress** especifica o recupera un valor que indica si se utilizará la barra de progreso en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="6c9b9-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6c9b9-106">Possible Values</span></span>

<span data-ttu-id="6c9b9-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="6c9b9-108">Value</span><span class="sxs-lookup"><span data-stu-id="6c9b9-108">Value</span></span> | <span data-ttu-id="6c9b9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c9b9-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="6c9b9-110">true</span><span class="sxs-lookup"><span data-stu-id="6c9b9-110">true</span></span>  | <span data-ttu-id="6c9b9-111">Usar el progreso en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="6c9b9-112">false</span><span class="sxs-lookup"><span data-stu-id="6c9b9-112">false</span></span> | <span data-ttu-id="6c9b9-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-113">Default.</span></span> <span data-ttu-id="6c9b9-114">No usar el progreso en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c9b9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c9b9-115">Remarks</span></span>

<span data-ttu-id="6c9b9-116">Este atributo permite el uso del atributo **foregroundProgress** , que se usa principalmente para realizar el seguimiento del progreso de la descarga de un archivo multimedia mientras se realiza un seguimiento simultáneo de la posición de reproducción actual del archivo mediante el atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="6c9b9-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9b9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c9b9-117">Requirements</span></span>



| <span data-ttu-id="6c9b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c9b9-118">Requirement</span></span> | <span data-ttu-id="6c9b9-119">Value</span><span class="sxs-lookup"><span data-stu-id="6c9b9-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6c9b9-120">Versión</span><span class="sxs-lookup"><span data-stu-id="6c9b9-120">Version</span></span><br/> | <span data-ttu-id="6c9b9-121">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6c9b9-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c9b9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c9b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9b9-123">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="6c9b9-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="6c9b9-124">**SLIDEr. foregroundProgress**</span><span class="sxs-lookup"><span data-stu-id="6c9b9-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="6c9b9-125">**Control deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="6c9b9-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





