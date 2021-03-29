---
description: El descodificador de vídeo DV Media Foundation es una transformación Media Foundation que descodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Descodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808095"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="a2d22-103">Descodificador de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="a2d22-103">DV Video Decoder</span></span>

<span data-ttu-id="a2d22-104">El descodificador de vídeo DV Media Foundation es una [transformación Media Foundation](media-foundation-transforms.md) que DESCODIFICA vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="a2d22-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="a2d22-105">El descodificador de vídeo DV admite los siguientes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="a2d22-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="a2d22-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="a2d22-106">Subtype</span></span>                 | <span data-ttu-id="a2d22-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2d22-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="a2d22-108">**MFVideoFormat \_ DVC**</span><span class="sxs-lookup"><span data-stu-id="a2d22-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="a2d22-109">Vídeo de DVC/DV</span><span class="sxs-lookup"><span data-stu-id="a2d22-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="a2d22-110">**MFVideoFormat \_ DVHD**</span><span class="sxs-lookup"><span data-stu-id="a2d22-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="a2d22-111">HD-DVCR (1125-60 o 1250-50)</span><span class="sxs-lookup"><span data-stu-id="a2d22-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="a2d22-112">**MFVideoFormat \_ DVSD**</span><span class="sxs-lookup"><span data-stu-id="a2d22-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="a2d22-113">SDL-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="a2d22-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="a2d22-114">**MFVideoFormat \_ DVSL**</span><span class="sxs-lookup"><span data-stu-id="a2d22-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="a2d22-115">SD-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="a2d22-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="a2d22-116">Admite un solo tipo de salida:</span><span class="sxs-lookup"><span data-stu-id="a2d22-116">It supports a single output type:</span></span>



| <span data-ttu-id="a2d22-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="a2d22-117">Subtype</span></span>             | <span data-ttu-id="a2d22-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2d22-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="a2d22-119">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="a2d22-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="a2d22-120">Vídeo de YUY2</span><span class="sxs-lookup"><span data-stu-id="a2d22-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="a2d22-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2d22-121">Requirements</span></span>



| <span data-ttu-id="a2d22-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2d22-122">Requirement</span></span> | <span data-ttu-id="a2d22-123">Value</span><span class="sxs-lookup"><span data-stu-id="a2d22-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d22-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d22-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d22-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2d22-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2d22-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d22-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d22-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2d22-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2d22-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2d22-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2d22-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2d22-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d22-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2d22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d22-131">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="a2d22-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a2d22-132">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2d22-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a2d22-133">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="a2d22-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




