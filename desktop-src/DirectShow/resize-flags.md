---
description: Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Marcas de redimensionamiento (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690711"
---
# <a name="resize-flags"></a><span data-ttu-id="0ebc7-103">Cambiar el tamaño de las marcas</span><span class="sxs-lookup"><span data-stu-id="0ebc7-103">Resize Flags</span></span>

<span data-ttu-id="0ebc7-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-104">\[Deprecated.</span></span> <span data-ttu-id="0ebc7-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ebc7-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="0ebc7-106">Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="0ebc7-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="0ebc7-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="0ebc7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ebc7-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="0ebc7-109"><dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc7-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="0ebc7-110">La imagen se ajusta para ajustarse al tamaño del marco de destino en ambas dimensiones, sin conservar la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="0ebc7-111"><dt>**RESIZEF \_ Recortar**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc7-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="0ebc7-112">No se cambia el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-112">The image is not resized.</span></span> <span data-ttu-id="0ebc7-113">Si la imagen es más pequeña que el marco de destino, el área circundante es negro.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="0ebc7-114">Si la imagen es mayor que el marco de destino, se recorta la imagen.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="0ebc7-115"><dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc7-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="0ebc7-116">Se cambia el tamaño de la imagen para ajustarse al marco de destino a lo largo de una dimensión, a la vez que se conserva la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="0ebc7-117">Si la relación entre el ancho y el alto de la imagen no coincide con la relación en el marco de destino, se crea una pantalla panorámica.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="0ebc7-118"><dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ noancha**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc7-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0ebc7-119">Se cambia el tamaño de la imagen para rellenar todo el marco de destino al tiempo que se conserva la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="0ebc7-120">En lugar de crear una panorámica, este modo recorta la imagen, ya sea a lo largo de los lados o en la parte superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="0ebc7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ebc7-121">Remarks</span></span>

<span data-ttu-id="0ebc7-122">En las siguientes imágenes se muestran los efectos de estas marcas.</span><span class="sxs-lookup"><span data-stu-id="0ebc7-122">The following images show the effects of these flags.</span></span>

![cambiar el tamaño de las marcas](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="0ebc7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebc7-124">Requirements</span></span>



| <span data-ttu-id="0ebc7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebc7-125">Requirement</span></span> | <span data-ttu-id="0ebc7-126">Value</span><span class="sxs-lookup"><span data-stu-id="0ebc7-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebc7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ebc7-127">Header</span></span><br/> | <dl> <span data-ttu-id="0ebc7-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc7-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebc7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ebc7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebc7-130">**IAMTimelineSrc::GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="0ebc7-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="0ebc7-131">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="0ebc7-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




