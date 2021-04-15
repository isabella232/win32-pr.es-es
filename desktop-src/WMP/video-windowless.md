---
title: VÍDEO. sin ventanas
description: El atributo sin ventana especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VÍDEO Media Player ventanas sin ventanas
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708880"
---
# <a name="videowindowless"></a><span data-ttu-id="6ed83-104">VÍDEO. sin ventanas</span><span class="sxs-lookup"><span data-stu-id="6ed83-104">VIDEO.windowless</span></span>

<span data-ttu-id="6ed83-105">El atributo **sin ventana** especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar.</span><span class="sxs-lookup"><span data-stu-id="6ed83-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="6ed83-106">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="6ed83-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="6ed83-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6ed83-107">Possible Values</span></span>

<span data-ttu-id="6ed83-108">Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura después.</span><span class="sxs-lookup"><span data-stu-id="6ed83-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="6ed83-109">Value</span><span class="sxs-lookup"><span data-stu-id="6ed83-109">Value</span></span> | <span data-ttu-id="6ed83-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ed83-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="6ed83-111">true</span><span class="sxs-lookup"><span data-stu-id="6ed83-111">true</span></span>  | <span data-ttu-id="6ed83-112">El control de vídeo no tendrá ventanas.</span><span class="sxs-lookup"><span data-stu-id="6ed83-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="6ed83-113">false</span><span class="sxs-lookup"><span data-stu-id="6ed83-113">false</span></span> | <span data-ttu-id="6ed83-114">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6ed83-114">Default.</span></span> <span data-ttu-id="6ed83-115">El control de vídeo se mostrará en una ventana.</span><span class="sxs-lookup"><span data-stu-id="6ed83-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6ed83-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ed83-116">Remarks</span></span>

<span data-ttu-id="6ed83-117">Si se desea una ventana de vídeo no rectangular, o si quiere cubrir cualquier parte de la ventana de vídeo con una imagen, este atributo debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="6ed83-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="6ed83-118">Esto sacrifica algún rendimiento para realizar el recorte necesario.</span><span class="sxs-lookup"><span data-stu-id="6ed83-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="6ed83-119">La reproducción de vídeo está optimizada para la reproducción no recortada.</span><span class="sxs-lookup"><span data-stu-id="6ed83-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="6ed83-120">En este caso, el atributo **Windowless** está establecido en false y siempre se muestra el rectángulo de vídeo completo.</span><span class="sxs-lookup"><span data-stu-id="6ed83-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="6ed83-121">Se omite cualquier imagen que abarque la ventana de vídeo y la ventana de vídeo tiene el orden z de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="6ed83-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed83-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed83-122">Requirements</span></span>



| <span data-ttu-id="6ed83-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed83-123">Requirement</span></span> | <span data-ttu-id="6ed83-124">Value</span><span class="sxs-lookup"><span data-stu-id="6ed83-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6ed83-125">Versión</span><span class="sxs-lookup"><span data-stu-id="6ed83-125">Version</span></span><br/> | <span data-ttu-id="6ed83-126">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6ed83-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ed83-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ed83-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed83-128">**Elemento de vídeo**</span><span class="sxs-lookup"><span data-stu-id="6ed83-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





