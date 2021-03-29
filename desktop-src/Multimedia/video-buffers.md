---
title: Búferes de vídeo
description: Búferes de vídeo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778120"
---
# <a name="video-buffers"></a><span data-ttu-id="d42dd-107">Búferes de vídeo</span><span class="sxs-lookup"><span data-stu-id="d42dd-107">Video Buffers</span></span>

<span data-ttu-id="d42dd-108">Los búferes que se usan con la captura de vídeo residen en el montón de memoria.</span><span class="sxs-lookup"><span data-stu-id="d42dd-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="d42dd-109">El número de búferes utilizados en una operación de captura puede variar y depender del valor del miembro **wNumVideoRequested** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) y de la memoria disponible del sistema.</span><span class="sxs-lookup"><span data-stu-id="d42dd-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="d42dd-110">Puede recuperar el valor actual de los búferes de vídeo solicitados mediante el mensaje de configuración de la [**\_ secuencia de \_ \_ salida \_ Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="d42dd-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="d42dd-111">El número solicitado actual de búferes de vídeo se almacena en el miembro **wNumVideoRequested** de la estructura **CAPTUREPARMS** .</span><span class="sxs-lookup"><span data-stu-id="d42dd-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="d42dd-112">Puede solicitar la ubicación y el número de búferes si actualiza este miembro y, a continuación, envía la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) definición de Cap de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="d42dd-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




