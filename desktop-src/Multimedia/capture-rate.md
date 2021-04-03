---
title: Velocidad de captura
description: Velocidad de captura
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075723"
---
# <a name="capture-rate"></a><span data-ttu-id="b2f1f-108">Velocidad de captura</span><span class="sxs-lookup"><span data-stu-id="b2f1f-108">Capture Rate</span></span>

<span data-ttu-id="b2f1f-109">La velocidad de captura es el número de fotogramas que se capturan cada segundo de una sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="b2f1f-110">Puede recuperar la velocidad de captura actual mediante el mensaje de configuración de la [**\_ \_ \_ \_ secuencia Get Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="b2f1f-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="b2f1f-111">La velocidad de captura actual se almacena en el miembro **dwRequestMicroSecPerFrame** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="b2f1f-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="b2f1f-112">Puede establecer la velocidad de captura si especifica el número de microsegundos entre fotogramas sucesivos como el valor de este miembro y, a continuación, envía la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) la secuencia del conjunto de límites de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="b2f1f-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="b2f1f-113">El valor predeterminado de **dwRequestMicroSecPerFrame** es 66667, que corresponde a 15 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 




