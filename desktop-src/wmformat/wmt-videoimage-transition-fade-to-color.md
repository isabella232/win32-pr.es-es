---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transición de fundido a color se resuelve de la imagen en un marco de color sólido.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699584"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="4ecd9-104">\_ \_ transición de imagen de transmisión de imágenes WMT \_ \_ a \_ color</span><span class="sxs-lookup"><span data-stu-id="4ecd9-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="4ecd9-105">La transición de fundido a color se resuelve de la imagen en un marco de color sólido.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ecd9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ecd9-106">Parameters</span></span>

<span data-ttu-id="4ecd9-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="4ecd9-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4ecd9-108">Parameter</span></span>         | <span data-ttu-id="4ecd9-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="4ecd9-109">Structure member</span></span> | <span data-ttu-id="4ecd9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ecd9-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecd9-111">Rojo</span><span class="sxs-lookup"><span data-stu-id="4ecd9-111">Red</span></span>               | <span data-ttu-id="4ecd9-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="4ecd9-112">**fEffectPara0**</span></span> | <span data-ttu-id="4ecd9-113">Valor rojo del color de fondo.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-113">Red value of the background color.</span></span> <span data-ttu-id="4ecd9-114">Establezca en un número comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="4ecd9-115">Verde</span><span class="sxs-lookup"><span data-stu-id="4ecd9-115">Green</span></span>             | <span data-ttu-id="4ecd9-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="4ecd9-116">**fEffectPara1**</span></span> | <span data-ttu-id="4ecd9-117">Valor verde del color de fondo.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-117">Green value of the background color.</span></span> <span data-ttu-id="4ecd9-118">Establezca en un número comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="4ecd9-119">Azul</span><span class="sxs-lookup"><span data-stu-id="4ecd9-119">Blue</span></span>              | <span data-ttu-id="4ecd9-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="4ecd9-120">**fEffectPara2**</span></span> | <span data-ttu-id="4ecd9-121">Valor azul del color de fondo.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-121">Blue value of the background color.</span></span> <span data-ttu-id="4ecd9-122">Establezca en un número comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="4ecd9-123">Peso de fondo</span><span class="sxs-lookup"><span data-stu-id="4ecd9-123">Background weight</span></span> | <span data-ttu-id="4ecd9-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="4ecd9-124">**fEffectPara3**</span></span> | <span data-ttu-id="4ecd9-125">Peso del color de fondo.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-125">Weight of the background color.</span></span> <span data-ttu-id="4ecd9-126">Este parámetro expresa el porcentaje del color de fondo de la combinación como un decimal.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="4ecd9-127">Por ejemplo, para mezclar el color de fondo en un 30%, lo que permite que la imagen del 70% de la combinación se establezca en 0,30.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4ecd9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ecd9-128">Requirements</span></span>



| <span data-ttu-id="4ecd9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ecd9-129">Requirement</span></span> | <span data-ttu-id="4ecd9-130">Value</span><span class="sxs-lookup"><span data-stu-id="4ecd9-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecd9-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ecd9-131">Header</span></span><br/> | <dl> <span data-ttu-id="4ecd9-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecd9-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecd9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ecd9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecd9-134">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="4ecd9-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





