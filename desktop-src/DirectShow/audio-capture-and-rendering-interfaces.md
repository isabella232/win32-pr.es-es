---
description: Interfaces de representación y captura de audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de representación y captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677183"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="a0d94-103">Interfaces de representación y captura de audio</span><span class="sxs-lookup"><span data-stu-id="a0d94-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="a0d94-104">Estas interfaces admiten la captura y representación de audio en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0d94-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="a0d94-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="a0d94-105">Interface</span></span>                                              | <span data-ttu-id="a0d94-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0d94-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0d94-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="a0d94-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="a0d94-108">Obtener acceso a las entradas analógicas de la tarjeta de sonido del sistema y ajustar características, como mono o estéreo, nivel de combinación, nivel de pan, sonoridad, agudos y graves.</span><span class="sxs-lookup"><span data-stu-id="a0d94-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="a0d94-109">**IAMAudioRendererStats**</span><span class="sxs-lookup"><span data-stu-id="a0d94-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="a0d94-110">Obtenga información estadística sobre el rendimiento de renderering de audio.</span><span class="sxs-lookup"><span data-stu-id="a0d94-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="a0d94-111">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="a0d94-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="a0d94-112">Controlan cómo el filtro de captura de audio asigna los búferes.</span><span class="sxs-lookup"><span data-stu-id="a0d94-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="a0d94-113">**IAMClockSlave**</span><span class="sxs-lookup"><span data-stu-id="a0d94-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="a0d94-114">Controlar la tolerancia de un representador de audio cuando coincide con las tarifas con otro reloj.</span><span class="sxs-lookup"><span data-stu-id="a0d94-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="a0d94-115">**IAMDirectSound**</span><span class="sxs-lookup"><span data-stu-id="a0d94-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="a0d94-116">Permite a una aplicación especificar qué ventana tiene el foco para controlar la reproducción de audio de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="a0d94-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="a0d94-117">**IAMResourceControl**</span><span class="sxs-lookup"><span data-stu-id="a0d94-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="a0d94-118">Conserve un recurso de dispositivo de audio antes de que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a0d94-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="a0d94-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="a0d94-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="a0d94-120">Consulta y establece el formato de salida del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="a0d94-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="a0d94-121">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="a0d94-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="a0d94-122">Establezca el volumen y el equilibrio de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="a0d94-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="a0d94-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0d94-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d94-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a0d94-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



