---
title: Acceso y control de los datos de los marcos de DWM
description: En este tema se describen las API de Administrador de ventanas de escritorio (DWM) que se usan para la programación y la presentación multimedia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Administrador de ventanas de escritorio (DWM), programación y API de presentación multimedia
- DWM (Administrador de ventanas de escritorio), programación y API de presentación multimedia
- programación y API de presentación multimedia
- Administrador de ventanas de escritorio (DWM), obtener acceso a los datos del marco
- DWM (Administrador de ventanas de escritorio), acceso a los datos del marco
- obtener acceso a los datos del marco
- Administrador de ventanas de escritorio (DWM), controlar los datos del marco
- DWM (Administrador de ventanas de escritorio), controlar los datos del marco
- controlar los datos del marco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357173"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="2e4bb-112">Acceso y control de los datos de los marcos de DWM</span><span class="sxs-lookup"><span data-stu-id="2e4bb-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="2e4bb-113">En este tema se describen las API de Administrador de ventanas de escritorio (DWM) que se usan para la programación y la presentación multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="2e4bb-114">API de temporización de fotogramas de DWM</span><span class="sxs-lookup"><span data-stu-id="2e4bb-114">DWM Frame Timing API</span></span>

<span data-ttu-id="2e4bb-115">Las API de programación y presentación multimedia permiten un control más detallado de Cuándo se compone y se presenta la imagen de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="2e4bb-116">Normalmente, esto es necesario para las aplicaciones de reproducción multimedia y de vídeo para las que el DWM se ejecuta de forma asincrónica con su propia programación de presentación, lo que puede conducir a los artefactos de muestreo si no se controlan estrechamente.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="2e4bb-117">Entre las funciones de presentación multimedia y programación se incluyen las siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="2e4bb-118">Los detalles de su uso se encuentran en esas páginas.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="2e4bb-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="2e4bb-120">Notifica a DWM que habilite la programación del servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="2e4bb-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="2e4bb-122">Recupera la información de tiempo de composición actual.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="2e4bb-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="2e4bb-124">Cambia el número de actualizaciones durante las cuales se mostrará el fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="2e4bb-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="2e4bb-126">Establece el número de actualizaciones en las que se va a mostrar el marco presentado.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="2e4bb-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="2e4bb-128">Establece los parámetros presentes para la composición de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-128">Sets the present parameters for frame composition.</span></span>

 

 




