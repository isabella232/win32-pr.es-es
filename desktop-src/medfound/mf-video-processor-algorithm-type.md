---
description: Define los algoritmos para el procesador de vídeo que usa el \_ algoritmo del procesador de vídeo MF \_ \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumeración MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696632"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="b9ae1-103">\_ \_ \_ Enumeración de tipo de algoritmo del procesador de vídeo MF \_</span><span class="sxs-lookup"><span data-stu-id="b9ae1-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="b9ae1-104">Define los algoritmos para el procesador de vídeo que usa [el \_ \_ \_ algoritmo del procesador de vídeo MF](mf-video-processor-algorithm.md).</span><span class="sxs-lookup"><span data-stu-id="b9ae1-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ae1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9ae1-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b9ae1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b9ae1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b9ae1-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_algoritmo de procesador de vídeo MF \_ \_ \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="b9ae1-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="b9ae1-108">el modo predeterminado favorece un equilibrio de calidad y velocidad</span><span class="sxs-lookup"><span data-stu-id="b9ae1-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="b9ae1-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo del procesador de vídeo MF \_ \_ \_ MRF \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="b9ae1-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="b9ae1-110">El procesador de vídeo siempre procesará internamente en AYUV y usará filtros de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="b9ae1-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9ae1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ae1-111">Requirements</span></span>



| <span data-ttu-id="b9ae1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ae1-112">Requirement</span></span> | <span data-ttu-id="b9ae1-113">Value</span><span class="sxs-lookup"><span data-stu-id="b9ae1-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ae1-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ae1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ae1-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b9ae1-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9ae1-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ae1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ae1-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9ae1-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9ae1-118">IDL</span><span class="sxs-lookup"><span data-stu-id="b9ae1-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9ae1-119"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9ae1-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ae1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ae1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ae1-121">Enumeraciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9ae1-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




