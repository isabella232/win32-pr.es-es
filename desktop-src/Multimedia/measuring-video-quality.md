---
title: Medición de la calidad del vídeo
description: Medición de la calidad del vídeo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075648"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="c7e6f-107">Medición de la calidad del vídeo</span><span class="sxs-lookup"><span data-stu-id="c7e6f-107">Measuring Video Quality</span></span>

<span data-ttu-id="c7e6f-108">Una manera de medir la calidad del vídeo es limitar el número de fotogramas capturados quitados durante la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="c7e6f-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="c7e6f-109">Una vez finalizada la captura de streaming, el valor de calidad se compara con la relación de fotogramas quitados con el total de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="c7e6f-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="c7e6f-110">Si el porcentaje de fotogramas quitados es mayor que el valor del miembro **wPercentDropForError** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap envía un mensaje de error a la función de devolución de llamada de error si está instalada.</span><span class="sxs-lookup"><span data-stu-id="c7e6f-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="c7e6f-111">Puede recuperar el límite actual de fotogramas quitados (expresado como un porcentaje) mediante el mensaje de configuración de la secuencia de obtención de Cap de WM (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). [**\_ \_ \_ \_**](wm-cap-get-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="c7e6f-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="c7e6f-112">Puede establecer un límite nuevo especificando un porcentaje como el valor del miembro **wPercentDropForError** de la estructura **CAPTUREPARMS** y, a continuación, enviando la estructura actualizada a la ventana de captura mediante el mensaje de configuración de la [**\_ \_ \_ secuencia \_ de límite de Cap de WM**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="c7e6f-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="c7e6f-113">El valor predeterminado de **wPercentDropForError** es 10 por ciento.</span><span class="sxs-lookup"><span data-stu-id="c7e6f-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




