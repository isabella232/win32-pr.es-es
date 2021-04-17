---
description: Estructuras de audio principales
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estructuras de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659317"
---
# <a name="core-audio-structures"></a><span data-ttu-id="047f6-103">Estructuras de audio principales</span><span class="sxs-lookup"><span data-stu-id="047f6-103">Core Audio Structures</span></span>

<span data-ttu-id="047f6-104">En esta sección se describen las estructuras utilizadas por las API de audio principales en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="047f6-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="047f6-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="047f6-105">Structure</span></span>                                                                     | <span data-ttu-id="047f6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="047f6-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="047f6-107">**\_datos de \_ notificación por volumen de audio \_**</span><span class="sxs-lookup"><span data-stu-id="047f6-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="047f6-108">Describe un cambio en el nivel de volumen o el estado de silenciación de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="047f6-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="047f6-109">**\_parámetros de \_ activación de audio de DirectX \_**</span><span class="sxs-lookup"><span data-stu-id="047f6-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="047f6-110">Especifica los parámetros de inicialización de una secuencia DirectSound.</span><span class="sxs-lookup"><span data-stu-id="047f6-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="047f6-111">**Descripción de KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="047f6-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="047f6-112">Recuperado a través de [**IKsJackDescription:: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describe un conector de audio.</span><span class="sxs-lookup"><span data-stu-id="047f6-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="047f6-113">**KSJACK \_ DESCRIPTION2**</span><span class="sxs-lookup"><span data-stu-id="047f6-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="047f6-114">Recuperado a través de [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describe un conector de audio.</span><span class="sxs-lookup"><span data-stu-id="047f6-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="047f6-115">**\_información del receptor de KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="047f6-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="047f6-116">Recuperado a través de [**IKsJackSinkInformation:: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describe un receptor de conector de audio.</span><span class="sxs-lookup"><span data-stu-id="047f6-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="047f6-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="047f6-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="047f6-118">Almacena el identificador de puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="047f6-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="047f6-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="047f6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="047f6-120">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="047f6-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




