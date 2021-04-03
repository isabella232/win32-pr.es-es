---
title: Estructuras DWM
description: Esta sección contiene información sobre las estructuras Administrador de ventanas de escritorio (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), estructuras
- DWM (Administrador de ventanas de escritorio), estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075754"
---
# <a name="dwm-structures"></a><span data-ttu-id="0a09e-107">Estructuras DWM</span><span class="sxs-lookup"><span data-stu-id="0a09e-107">DWM Structures</span></span>

<span data-ttu-id="0a09e-108">Esta sección contiene información sobre las estructuras Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="0a09e-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0a09e-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0a09e-109">In this section</span></span>



| <span data-ttu-id="0a09e-110">Tema</span><span class="sxs-lookup"><span data-stu-id="0a09e-110">Topic</span></span>                                                                     | <span data-ttu-id="0a09e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a09e-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a09e-112">**BLURBEHIND de DWM \_**</span><span class="sxs-lookup"><span data-stu-id="0a09e-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="0a09e-113">Especifica las propiedades de desenfoque de DWM.</span><span class="sxs-lookup"><span data-stu-id="0a09e-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="0a09e-114">Lo utiliza la función [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) .</span><span class="sxs-lookup"><span data-stu-id="0a09e-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="0a09e-115">**\_parámetros presentes de DWM \_**</span><span class="sxs-lookup"><span data-stu-id="0a09e-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="0a09e-116">Especifica los parámetros del fotograma de vídeo de DWM para la composición de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0a09e-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="0a09e-117">Lo utiliza la función [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) .</span><span class="sxs-lookup"><span data-stu-id="0a09e-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="0a09e-118">**\_propiedades de miniatura de DWM \_**</span><span class="sxs-lookup"><span data-stu-id="0a09e-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="0a09e-119">Especifica las propiedades de miniatura de DWM.</span><span class="sxs-lookup"><span data-stu-id="0a09e-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="0a09e-120">Lo utiliza la función [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="0a09e-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="0a09e-121">**\_información de temporización de DWM \_**</span><span class="sxs-lookup"><span data-stu-id="0a09e-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="0a09e-122">Especifica la información de tiempo de composición de DWM.</span><span class="sxs-lookup"><span data-stu-id="0a09e-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="0a09e-123">Lo utiliza la función [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) .</span><span class="sxs-lookup"><span data-stu-id="0a09e-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="0a09e-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="0a09e-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="0a09e-125">Especifica una matriz de 3x2 que describe una transformación.</span><span class="sxs-lookup"><span data-stu-id="0a09e-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="0a09e-126">**relación sin signo \_**</span><span class="sxs-lookup"><span data-stu-id="0a09e-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="0a09e-127">Define un tipo de datos que usan las API de DWM.</span><span class="sxs-lookup"><span data-stu-id="0a09e-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="0a09e-128">Representa una relación genérica y se usa para diferentes propósitos y unidades incluso dentro de una sola API.</span><span class="sxs-lookup"><span data-stu-id="0a09e-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





