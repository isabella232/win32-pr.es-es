---
title: Búferes de audio
description: Búferes de audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774713"
---
# <a name="audio-buffers"></a><span data-ttu-id="e64a8-107">Búferes de audio</span><span class="sxs-lookup"><span data-stu-id="e64a8-107">Audio Buffers</span></span>

<span data-ttu-id="e64a8-108">Puede controlar la parte de audio de una operación de captura de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="e64a8-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="e64a8-109">Incluir o excluir audio de la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="e64a8-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="e64a8-110">Solicitar un número específico de búferes de audio.</span><span class="sxs-lookup"><span data-stu-id="e64a8-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="e64a8-111">Solicite que los búferes de audio tengan un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="e64a8-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="e64a8-112">Puede recuperar la configuración de los búferes de audio mediante el mensaje de configuración de la [**\_ secuencia de \_ \_ salida \_ de Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="e64a8-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="e64a8-113">El miembro **fCaptureAudio** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) especifica si el audio se incluye o se excluye de la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="e64a8-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="e64a8-114">El número solicitado actual de búferes de audio se almacena en el miembro **wNumAudioRequested** y el tamaño actual del búfer de audio se almacena en el miembro **dwAudioBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="e64a8-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="e64a8-115">Puede especificar si desea incluir la captura de audio, especificar el tamaño y el número de búferes de audio mediante la actualización de estos miembros y enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) secuencia del conjunto de Cap de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="e64a8-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="e64a8-116">De forma predeterminada, el audio se incluye en la operación de captura y se asignan cuatro búferes de audio.</span><span class="sxs-lookup"><span data-stu-id="e64a8-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="e64a8-117">El valor predeterminado de **fCaptureAudio** es **true**.</span><span class="sxs-lookup"><span data-stu-id="e64a8-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="e64a8-118">El tamaño de búfer predeterminado (el valor de **dwAudioBufferSize**) puede contener 0,5 segundos de datos de audio o 10 000, lo que sea mayor.</span><span class="sxs-lookup"><span data-stu-id="e64a8-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




