---
description: Estas marcas definen la configuración del procesador de vídeo (ProcAmp).
ms.assetid: 60d97b9e-d77c-4e53-94ea-ebd59c2601df
title: Configuración de ProcAmp (Dxva2api. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0181d7491d948a4ec4219ada4241397b8a721b0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677555"
---
# <a name="procamp-settings"></a><span data-ttu-id="74288-103">Configuración de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="74288-103">ProcAmp Settings</span></span>

<span data-ttu-id="74288-104">Estas marcas definen la configuración del procesador de vídeo (ProcAmp).</span><span class="sxs-lookup"><span data-stu-id="74288-104">These flags define video processor (ProcAmp) settings.</span></span>



| <span data-ttu-id="74288-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="74288-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="74288-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="74288-106">Description</span></span>           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|
| <span id="DXVA2_ProcAmp_None"></span><span id="dxva2_procamp_none"></span><span id="DXVA2_PROCAMP_NONE"></span><dl> <span data-ttu-id="74288-107"><dt>**DXVA2 \_ ProcAmp \_ ninguno**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="74288-107"><dt>**DXVA2\_ProcAmp\_None**</dt> <dt>0x0000</dt></span></span> </dl>                         | <span data-ttu-id="74288-108">None</span><span class="sxs-lookup"><span data-stu-id="74288-108">None</span></span><br/>       |
| <span id="DXVA2_ProcAmp_Brightness"></span><span id="dxva2_procamp_brightness"></span><span id="DXVA2_PROCAMP_BRIGHTNESS"></span><dl> <span data-ttu-id="74288-109"><dt>**DXVA2 \_ \_Brillo de ProcAmp**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="74288-109"><dt>**DXVA2\_ProcAmp\_Brightness**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="74288-110">Luminosidad</span><span class="sxs-lookup"><span data-stu-id="74288-110">Brightness</span></span><br/> |
| <span id="DXVA2_ProcAmp_Contrast"></span><span id="dxva2_procamp_contrast"></span><span id="DXVA2_PROCAMP_CONTRAST"></span><dl> <span data-ttu-id="74288-111"><dt>**DXVA2 \_ \_Contraste de ProcAmp**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="74288-111"><dt>**DXVA2\_ProcAmp\_Contrast**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="74288-112">Compare</span><span class="sxs-lookup"><span data-stu-id="74288-112">Contrast</span></span><br/>   |
| <span id="DXVA2_ProcAmp_Hue"></span><span id="dxva2_procamp_hue"></span><span id="DXVA2_PROCAMP_HUE"></span><dl> <span data-ttu-id="74288-113"><dt>**DXVA2 \_ ProcAmp \_ matiz**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="74288-113"><dt>**DXVA2\_ProcAmp\_Hue**</dt> <dt>0x0004</dt></span></span> </dl>                             | <span data-ttu-id="74288-114">Matiz</span><span class="sxs-lookup"><span data-stu-id="74288-114">Hue</span></span><br/>        |
| <span id="DXVA2_ProcAmp_Saturation"></span><span id="dxva2_procamp_saturation"></span><span id="DXVA2_PROCAMP_SATURATION"></span><dl> <span data-ttu-id="74288-115"><dt>**DXVA2 \_ 0x0008 de \_ saturación de ProcAmp**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74288-115"><dt>**DXVA2\_ProcAmp\_Saturation**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="74288-116">Saturación</span><span class="sxs-lookup"><span data-stu-id="74288-116">Saturation</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="74288-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74288-117">Requirements</span></span>



| <span data-ttu-id="74288-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="74288-118">Requirement</span></span> | <span data-ttu-id="74288-119">Value</span><span class="sxs-lookup"><span data-stu-id="74288-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74288-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74288-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74288-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74288-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74288-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74288-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74288-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="74288-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74288-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74288-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74288-125"><dt>Dxva2api. h</dt></span><span class="sxs-lookup"><span data-stu-id="74288-125"><dt>Dxva2api.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74288-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="74288-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74288-127">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74288-127">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




