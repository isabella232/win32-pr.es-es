---
description: En el caso de un formato de vídeo 3D, especifica qué vista es la vista base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678285"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="a33f0-103">MF \_ MT \_ vídeo \_ 3D a la \_ izquierda \_ es el \_ atributo base</span><span class="sxs-lookup"><span data-stu-id="a33f0-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="a33f0-104">En el caso de un formato de vídeo 3D, especifica qué vista es la vista base.</span><span class="sxs-lookup"><span data-stu-id="a33f0-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="a33f0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a33f0-105">Data type</span></span>

<span data-ttu-id="a33f0-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a33f0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a33f0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a33f0-107">Remarks</span></span>

<span data-ttu-id="a33f0-108">De forma predeterminada, la vista izquierda en una secuencia de vídeo 3D es la vista base.</span><span class="sxs-lookup"><span data-stu-id="a33f0-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="a33f0-109">Si la vista de la derecha es la vista base, establezca este atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="a33f0-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="a33f0-110">Para convertir Stereoscopic video en 2D, mantenga la vista base y descarte la otra vista.</span><span class="sxs-lookup"><span data-stu-id="a33f0-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33f0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33f0-111">Requirements</span></span>



| <span data-ttu-id="a33f0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33f0-112">Requirement</span></span> | <span data-ttu-id="a33f0-113">Value</span><span class="sxs-lookup"><span data-stu-id="a33f0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f0-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33f0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a33f0-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="a33f0-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a33f0-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33f0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a33f0-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a33f0-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a33f0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a33f0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33f0-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33f0-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33f0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a33f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33f0-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a33f0-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




