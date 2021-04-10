---
title: Constantes y enumeraciones de DWM
description: Esta sección contiene información sobre las constantes y enumeraciones utilizadas en las API de Administrador de ventanas de escritorio (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), constantes
- DWM (Administrador de ventanas de escritorio), constantes
- Administrador de ventanas de escritorio (DWM), enumeraciones
- DWM (Administrador de ventanas de escritorio), enumeraciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776722"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="043fd-109">Constantes y enumeraciones de DWM</span><span class="sxs-lookup"><span data-stu-id="043fd-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="043fd-110">Esta sección contiene información sobre las constantes y enumeraciones utilizadas en las API de Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="043fd-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="043fd-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="043fd-111">In this section</span></span>



| <span data-ttu-id="043fd-112">Tema</span><span class="sxs-lookup"><span data-stu-id="043fd-112">Topic</span></span>                                                                                     | <span data-ttu-id="043fd-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="043fd-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="043fd-114">**Desenfoque de DWM detrás de constantes**</span><span class="sxs-lookup"><span data-stu-id="043fd-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="043fd-115">Marcas usadas por la [**estructura \_ BLURBEHIND de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar cuál de sus miembros contiene información válida.</span><span class="sxs-lookup"><span data-stu-id="043fd-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="043fd-116">**DWM habilitar constantes de composición**</span><span class="sxs-lookup"><span data-stu-id="043fd-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="043fd-117">Marcas usadas por la función [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  para cambiar el estado de la composición DWM.</span><span class="sxs-lookup"><span data-stu-id="043fd-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="043fd-118">**\_muestreo de \_ fotogramas de origen de DWM \_**</span><span class="sxs-lookup"><span data-stu-id="043fd-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="043fd-119">Marcas usadas por la función [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) para especificar el tipo de muestreo de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="043fd-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="043fd-120">**requisitos de la ventana de pestaña de DWM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="043fd-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="043fd-121">Devuelto por DwmGetUnmetTabRequirements para indicar los requisitos necesarios para que una ventana Coloque las pestañas en la barra de título de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="043fd-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="043fd-122">**\_Constantes TNP de DWM**</span><span class="sxs-lookup"><span data-stu-id="043fd-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="043fd-123">Marcas usadas por la estructura de [**\_ \_ propiedades de miniatura de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) para indicar cuál de sus miembros contiene información válida.</span><span class="sxs-lookup"><span data-stu-id="043fd-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="043fd-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="043fd-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="043fd-125">Marcas usadas por la función [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar la Directiva de la ventana de Flip3D.</span><span class="sxs-lookup"><span data-stu-id="043fd-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="043fd-126">**DWMNCRENDERINGPOLICY**</span><span class="sxs-lookup"><span data-stu-id="043fd-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="043fd-127">Marcas usadas por la función [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar la Directiva de representación de área no cliente.</span><span class="sxs-lookup"><span data-stu-id="043fd-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="043fd-128">**destino de DWMTRANSITION \_ OWNEDWINDOW \_**</span><span class="sxs-lookup"><span data-stu-id="043fd-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="043fd-129">Identifica el destino.</span><span class="sxs-lookup"><span data-stu-id="043fd-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="043fd-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="043fd-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="043fd-131">Marcas usadas por las funciones [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) y [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar atributos de ventana para la representación no cliente.</span><span class="sxs-lookup"><span data-stu-id="043fd-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="043fd-132">**tipo de gesto \_**</span><span class="sxs-lookup"><span data-stu-id="043fd-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="043fd-133">Identifica el tipo de gesto especificado en [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span><span class="sxs-lookup"><span data-stu-id="043fd-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





