---
description: Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705901"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="4b1b8-103">\_Atributo 3DVideo de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="4b1b8-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="4b1b8-104">Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.</span><span class="sxs-lookup"><span data-stu-id="4b1b8-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b1b8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4b1b8-105">Data type</span></span>

<span data-ttu-id="4b1b8-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4b1b8-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4b1b8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b1b8-107">Remarks</span></span>

<span data-ttu-id="4b1b8-108">Si este atributo es **true**, el ejemplo multimedia contiene un fotograma de vídeo que tiene dos o más vistas Stereoscopic.</span><span class="sxs-lookup"><span data-stu-id="4b1b8-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="4b1b8-109">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4b1b8-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="4b1b8-110">Un componente que genera fotogramas de vídeo 3D debe establecer este atributo en **true** en cada ejemplo multimedia que contenga un fotograma 3D.</span><span class="sxs-lookup"><span data-stu-id="4b1b8-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b1b8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1b8-111">Requirements</span></span>



| <span data-ttu-id="4b1b8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1b8-112">Requirement</span></span> | <span data-ttu-id="4b1b8-113">Value</span><span class="sxs-lookup"><span data-stu-id="4b1b8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1b8-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b1b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4b1b8-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="4b1b8-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4b1b8-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b1b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4b1b8-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="4b1b8-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4b1b8-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b1b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b1b8-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b1b8-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b1b8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b1b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b1b8-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b1b8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b1b8-122">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="4b1b8-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




