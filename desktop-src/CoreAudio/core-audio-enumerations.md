---
description: Enumeraciones de audio principales
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Enumeraciones de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496691"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="231fd-103">Enumeraciones de audio principales</span><span class="sxs-lookup"><span data-stu-id="231fd-103">Core Audio Enumerations</span></span>

<span data-ttu-id="231fd-104">En esta sección se describen las enumeraciones que utilizan las API de audio principales en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="231fd-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="231fd-105">Enumeración</span><span class="sxs-lookup"><span data-stu-id="231fd-105">Enumeration</span></span>                                                                   | <span data-ttu-id="231fd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="231fd-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="231fd-107">**\_AUDCLNT \_ BUFFERFLAGS**</span><span class="sxs-lookup"><span data-stu-id="231fd-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="231fd-108">Marcas de estado para un búfer de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="231fd-109">**AUDCLNT \_ SHAREMODE**</span><span class="sxs-lookup"><span data-stu-id="231fd-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="231fd-110">Modo de uso compartido de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="231fd-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="231fd-111">**AUDCLNT \_ STREAMOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="231fd-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="231fd-112">Define valores que describen las características de una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="231fd-113">**\_categoría de secuencia de audio \_**</span><span class="sxs-lookup"><span data-stu-id="231fd-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="231fd-114">Especifica la categoría de una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="231fd-115">**AudioSessionState**</span><span class="sxs-lookup"><span data-stu-id="231fd-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="231fd-116">El estado de una sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="231fd-117">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="231fd-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="231fd-118">El tipo de conector en una topología de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="231fd-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="231fd-119">**Flujo**</span><span class="sxs-lookup"><span data-stu-id="231fd-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="231fd-120">Dirección del flujo de datos de una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="231fd-121">**EDataFlow**</span><span class="sxs-lookup"><span data-stu-id="231fd-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="231fd-122">Dirección en la que los datos de audio fluyen entre un dispositivo de punto de conexión de audio y una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="231fd-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="231fd-123">**EndpointFormFactor**</span><span class="sxs-lookup"><span data-stu-id="231fd-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="231fd-124">Los atributos físicos generales de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="231fd-125">**ERole**</span><span class="sxs-lookup"><span data-stu-id="231fd-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="231fd-126">El rol de sistema de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="231fd-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="231fd-127">**\_CONNECTIONTYPE del receptor de KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="231fd-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="231fd-128">El tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="231fd-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="231fd-129">**PartType**</span><span class="sxs-lookup"><span data-stu-id="231fd-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="231fd-130">El tipo de parte de un elemento (conector o subunidad) en una topología de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="231fd-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="231fd-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="231fd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="231fd-132">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="231fd-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




