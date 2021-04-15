---
title: VÍDEO. zoom
description: El atributo zoom especifica el porcentaje por el que se va a escalar el vídeo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VÍDEO. zoom Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708150"
---
# <a name="videozoom"></a><span data-ttu-id="1b56f-104">VÍDEO. zoom</span><span class="sxs-lookup"><span data-stu-id="1b56f-104">VIDEO.zoom</span></span>

<span data-ttu-id="1b56f-105">El atributo **zoom** especifica el porcentaje por el que se va a escalar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b56f-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="1b56f-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1b56f-106">Possible Values</span></span>

<span data-ttu-id="1b56f-107">Este atributo es un **número** de lectura/escritura (**largo**) que va desde 1 hasta el tamaño máximo que se aloja en el ancho y el alto del control de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b56f-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="1b56f-108">Tiene un valor predeterminado de 100.</span><span class="sxs-lookup"><span data-stu-id="1b56f-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b56f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b56f-109">Remarks</span></span>

<span data-ttu-id="1b56f-110">Este atributo no se puede usar junto con el atributo de **pantalla completa** .</span><span class="sxs-lookup"><span data-stu-id="1b56f-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="1b56f-111">Si se especifican el **ancho** y el **alto** , y la ventana de vídeo resultante es mayor que el vídeo que se está reproduciendo, el vídeo se puede aumentar escalando hasta el tamaño máximo que se encuentra en la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b56f-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="1b56f-112">Si no se especifican el **ancho** y el **alto** , el **zoom** se limita a los valores de 100 o menos.</span><span class="sxs-lookup"><span data-stu-id="1b56f-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="1b56f-113">Si el valor de la propiedad **shrinkToFit** es false, el vídeo cambiará de proporción al zoom, para ajustarse al espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="1b56f-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="1b56f-114">Si **shrinkToFit** es true, el vídeo se reducirá para caber en la dimensión más restrictiva, a la vez que conserva sus proporciones originales.</span><span class="sxs-lookup"><span data-stu-id="1b56f-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b56f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b56f-115">Requirements</span></span>



| <span data-ttu-id="1b56f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b56f-116">Requirement</span></span> | <span data-ttu-id="1b56f-117">Value</span><span class="sxs-lookup"><span data-stu-id="1b56f-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1b56f-118">Versión</span><span class="sxs-lookup"><span data-stu-id="1b56f-118">Version</span></span><br/> | <span data-ttu-id="1b56f-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1b56f-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b56f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b56f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b56f-121">**Elemento de vídeo**</span><span class="sxs-lookup"><span data-stu-id="1b56f-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="1b56f-122">**VÍDEO. fullScreen**</span><span class="sxs-lookup"><span data-stu-id="1b56f-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="1b56f-123">**VÍDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="1b56f-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





