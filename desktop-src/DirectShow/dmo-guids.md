---
description: En la tabla siguiente se enumeran los identificadores únicos globales (GUID) definidos para las categorías de Microsoft DirectX media Object (DMO). Estos GUID se definen en el archivo de encabezado Dmoreg. h y se exportan mediante la biblioteca Dmoguids. lib.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: GUID de DMO (Dmoreg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653591"
---
# <a name="dmo-guids"></a><span data-ttu-id="e966e-104">GUID de DMO</span><span class="sxs-lookup"><span data-stu-id="e966e-104">DMO GUIDs</span></span>

<span data-ttu-id="e966e-105">En la tabla siguiente se enumeran los identificadores únicos globales (GUID) definidos para las categorías de Microsoft DirectX media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="e966e-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="e966e-106">Estos GUID se definen en el archivo de encabezado Dmoreg. h y se exportan mediante la biblioteca Dmoguids. lib.</span><span class="sxs-lookup"><span data-stu-id="e966e-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="e966e-107">Para enumerar el DMOs registrado en una categoría, pase el GUID correspondiente a la función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="e966e-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="e966e-108">GUID</span><span class="sxs-lookup"><span data-stu-id="e966e-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="e966e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e966e-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="e966e-110"><dt>**descodificador de audio de DMOCATEGORY \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="e966e-111">Descodificador de audio</span><span class="sxs-lookup"><span data-stu-id="e966e-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="e966e-112"><dt>**\_efecto de audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="e966e-113">Efecto de audio</span><span class="sxs-lookup"><span data-stu-id="e966e-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="e966e-114"><dt>**\_codificador de audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="e966e-115">Codificador de audio</span><span class="sxs-lookup"><span data-stu-id="e966e-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="e966e-116"><dt>**descodificador de vídeo de DMOCATEGORY \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="e966e-117">Descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e966e-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="e966e-118"><dt>**\_efecto de vídeo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="e966e-119">Efecto de vídeo</span><span class="sxs-lookup"><span data-stu-id="e966e-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="e966e-120"><dt>**\_codificador de vídeo de DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="e966e-121">Codificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e966e-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="e966e-122"><dt>**\_efecto de \_ captura de audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="e966e-123">Efecto de captura de audio</span><span class="sxs-lookup"><span data-stu-id="e966e-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e966e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e966e-124">Requirements</span></span>



| <span data-ttu-id="e966e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e966e-125">Requirement</span></span> | <span data-ttu-id="e966e-126">Value</span><span class="sxs-lookup"><span data-stu-id="e966e-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e966e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e966e-127">Header</span></span><br/> | <dl> <span data-ttu-id="e966e-128"><dt>Dmoreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e966e-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e966e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e966e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e966e-130">Constantes de DMO</span><span class="sxs-lookup"><span data-stu-id="e966e-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




