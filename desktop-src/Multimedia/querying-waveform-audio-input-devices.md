---
title: Consulta de dispositivos de entrada Waveform-Audio
description: Consulta de dispositivos de entrada Waveform-Audio
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio de onda, consulta de dispositivos de entrada
- 'onda: interfaz de audio, consulta de dispositivos de entrada'
- grabación de audio de onda, consulta de dispositivos de entrada
- consultar los dispositivos de entrada de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995193"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="264a7-107">Consulta de dispositivos de entrada Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="264a7-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="264a7-108">Antes de grabar audio de onda de onda, debe llamar a la función [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar las capacidades de entrada de audio de onda del sistema.</span><span class="sxs-lookup"><span data-stu-id="264a7-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="264a7-109">Esta función rellena una estructura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con información sobre las capacidades de un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="264a7-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="264a7-110">Esta información incluye los identificadores de fabricante y de producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="264a7-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="264a7-111">Además, la estructura **WAVEINCAPS** proporciona información sobre los formatos de audio de forma de onda estándar que admite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="264a7-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="264a7-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="264a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="264a7-113">Grabación de audio de onda</span><span class="sxs-lookup"><span data-stu-id="264a7-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 