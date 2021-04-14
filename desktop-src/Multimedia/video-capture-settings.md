---
title: Configuración de captura de vídeo
description: Configuración de captura de vídeo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665613"
---
# <a name="video-capture-settings"></a><span data-ttu-id="8f163-108">Configuración de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8f163-108">Video Capture Settings</span></span>

<span data-ttu-id="8f163-109">La estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene los parámetros de control para streaming de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f163-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="8f163-110">Esta estructura controla varios aspectos del proceso de captura y permite realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="8f163-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="8f163-111">Especifique la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8f163-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="8f163-112">Especifique el número de búferes de vídeo asignados.</span><span class="sxs-lookup"><span data-stu-id="8f163-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="8f163-113">Deshabilitar y habilitar la captura de audio.</span><span class="sxs-lookup"><span data-stu-id="8f163-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="8f163-114">Especifique el intervalo de tiempo para la captura.</span><span class="sxs-lookup"><span data-stu-id="8f163-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="8f163-115">Especifique si se usa un dispositivo MCI (VCR o videodisco) durante la captura.</span><span class="sxs-lookup"><span data-stu-id="8f163-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="8f163-116">Especifique el control del teclado o del mouse para finalizar el streaming.</span><span class="sxs-lookup"><span data-stu-id="8f163-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="8f163-117">Especifique el tipo de promedio de vídeo que se aplica durante la captura.</span><span class="sxs-lookup"><span data-stu-id="8f163-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="8f163-118">Puede recuperar la configuración de captura actual dentro de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) mediante el envío del mensaje de [**\_ \_ \_ \_ configuración de salida de Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="8f163-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="8f163-119">Puede establecer una o varias configuraciones de captura actuales si actualiza los miembros adecuados de la estructura **CAPTUREPARMS** y, a continuación, envía el mensaje de configuración de la secuencia de [**definición de Cap de WM \_ \_ \_ \_**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) y **CAPTUREPARMS** a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="8f163-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




