---
description: En el caso de un formato de vídeo 3D, especifica qué vista es la vista izquierda.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424056"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="23cb3-103">MF \_ MT \_ vídeo \_ 3D \_ primero \_ es el \_ atributo izquierdo</span><span class="sxs-lookup"><span data-stu-id="23cb3-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="23cb3-104">En el caso de un formato de vídeo 3D, especifica qué vista es la vista izquierda.</span><span class="sxs-lookup"><span data-stu-id="23cb3-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="23cb3-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="23cb3-105">Data type</span></span>

<span data-ttu-id="23cb3-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="23cb3-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="23cb3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23cb3-107">Remarks</span></span>

<span data-ttu-id="23cb3-108">En el caso de vídeo en 3D, cada ejemplo de vídeo contiene dos vistas, que se designan como *primera vista* y *segunda vista*.</span><span class="sxs-lookup"><span data-stu-id="23cb3-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="23cb3-109">El diseño exacto de las vistas en memoria se indica mediante el atributo de [ \_ \_ \_ \_ formato 3D de vídeo MF MT](mf-mt-video-3d-format.md) .</span><span class="sxs-lookup"><span data-stu-id="23cb3-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="23cb3-110">Formato</span><span class="sxs-lookup"><span data-stu-id="23cb3-110">Format</span></span>               | <span data-ttu-id="23cb3-111">Primera vista</span><span class="sxs-lookup"><span data-stu-id="23cb3-111">First View</span></span>              | <span data-ttu-id="23cb3-112">Segunda vista</span><span class="sxs-lookup"><span data-stu-id="23cb3-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="23cb3-113">Empaquetados en paralelo</span><span class="sxs-lookup"><span data-stu-id="23cb3-113">Packed side-by-side</span></span>  | <span data-ttu-id="23cb3-114">Mitad izquierda del búfer</span><span class="sxs-lookup"><span data-stu-id="23cb3-114">Left half of the buffer</span></span> | <span data-ttu-id="23cb3-115">Mitad derecha del búfer</span><span class="sxs-lookup"><span data-stu-id="23cb3-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="23cb3-116">Empaquetados de arriba abajo</span><span class="sxs-lookup"><span data-stu-id="23cb3-116">Packed top-to-bottom</span></span> | <span data-ttu-id="23cb3-117">Mitad superior del búfer</span><span class="sxs-lookup"><span data-stu-id="23cb3-117">Top half of the buffer</span></span>  | <span data-ttu-id="23cb3-118">Mitad inferior del búfer</span><span class="sxs-lookup"><span data-stu-id="23cb3-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="23cb3-119">MultiView</span><span class="sxs-lookup"><span data-stu-id="23cb3-119">Multiview</span></span>            | <span data-ttu-id="23cb3-120">Índice de búfer 0</span><span class="sxs-lookup"><span data-stu-id="23cb3-120">Buffer index 0</span></span>          | <span data-ttu-id="23cb3-121">Índice de búfer 1</span><span class="sxs-lookup"><span data-stu-id="23cb3-121">Buffer index 1</span></span>            |
| <span data-ttu-id="23cb3-122">Vista base</span><span class="sxs-lookup"><span data-stu-id="23cb3-122">Base view</span></span>            | <span data-ttu-id="23cb3-123">Fotograma completo</span><span class="sxs-lookup"><span data-stu-id="23cb3-123">Entire frame</span></span>            | <span data-ttu-id="23cb3-124">No está presente</span><span class="sxs-lookup"><span data-stu-id="23cb3-124">Not present</span></span>               |



 

<span data-ttu-id="23cb3-125">De forma predeterminada, la primera vista es la vista izquierda y la segunda vista es la derecha.</span><span class="sxs-lookup"><span data-stu-id="23cb3-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="23cb3-126">Si se intercambian las vistas izquierda y derecha, establezca el \_ atributo MF MT \_ video \_ 3D \_ First \_ is \_ left en **false** en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="23cb3-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="23cb3-127">En el formato de *vista base* (**MFVideo3DSampleFormat \_ BaseView**), solo se conserva la vista base, por lo que este atributo no se aplica.</span><span class="sxs-lookup"><span data-stu-id="23cb3-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23cb3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23cb3-128">Requirements</span></span>



| <span data-ttu-id="23cb3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cb3-129">Requirement</span></span> | <span data-ttu-id="23cb3-130">Value</span><span class="sxs-lookup"><span data-stu-id="23cb3-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23cb3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23cb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="23cb3-132">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="23cb3-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="23cb3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23cb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="23cb3-134">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="23cb3-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="23cb3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23cb3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="23cb3-136"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="23cb3-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23cb3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="23cb3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23cb3-138">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23cb3-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




