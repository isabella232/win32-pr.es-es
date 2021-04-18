---
title: VÍDEO. fullScreen
description: El atributo fullScreen especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VÍDEO de Windows. fullScreen Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709010"
---
# <a name="videofullscreen"></a><span data-ttu-id="5d10e-104">VÍDEO. fullScreen</span><span class="sxs-lookup"><span data-stu-id="5d10e-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="5d10e-105">El atributo **Fullscreen** especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5d10e-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="5d10e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5d10e-106">Possible Values</span></span>

<span data-ttu-id="5d10e-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="5d10e-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5d10e-108">Value</span><span class="sxs-lookup"><span data-stu-id="5d10e-108">Value</span></span> | <span data-ttu-id="5d10e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d10e-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="5d10e-110">true</span><span class="sxs-lookup"><span data-stu-id="5d10e-110">true</span></span>  | <span data-ttu-id="5d10e-111">El vídeo se muestra en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5d10e-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="5d10e-112">false</span><span class="sxs-lookup"><span data-stu-id="5d10e-112">false</span></span> | <span data-ttu-id="5d10e-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5d10e-113">Default.</span></span> <span data-ttu-id="5d10e-114">El vídeo no se muestra en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5d10e-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5d10e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d10e-115">Remarks</span></span>

<span data-ttu-id="5d10e-116">Esta propiedad solo se puede especificar en tiempo de ejecución, después de que se haya cargado un archivo.</span><span class="sxs-lookup"><span data-stu-id="5d10e-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="5d10e-117">Por lo tanto, debe establecerse en un controlador de eventos de script.</span><span class="sxs-lookup"><span data-stu-id="5d10e-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="5d10e-118">El botón escape se usa para volver a la vista normal.</span><span class="sxs-lookup"><span data-stu-id="5d10e-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d10e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d10e-119">Requirements</span></span>



| <span data-ttu-id="5d10e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d10e-120">Requirement</span></span> | <span data-ttu-id="5d10e-121">Value</span><span class="sxs-lookup"><span data-stu-id="5d10e-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5d10e-122">Versión</span><span class="sxs-lookup"><span data-stu-id="5d10e-122">Version</span></span><br/> | <span data-ttu-id="5d10e-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5d10e-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d10e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d10e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d10e-125">**Elemento de vídeo**</span><span class="sxs-lookup"><span data-stu-id="5d10e-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="5d10e-126">**VÍDEO. maintainAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="5d10e-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="5d10e-127">**VÍDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="5d10e-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="5d10e-128">**VÍDEO. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="5d10e-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





