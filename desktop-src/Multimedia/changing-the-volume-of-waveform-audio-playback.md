---
title: Cambiar el volumen de la reproducción de Waveform-Audio
description: Cambiar el volumen de la reproducción de Waveform-Audio
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio de una onda, cambio del volumen de reproducción
- 'onda: interfaz de audio, cambio del volumen de reproducción'
- audio de onda, volumen de reproducción
- 'onda: interfaz de audio, volumen de reproducción'
- cambiar el volumen de reproducción de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791637"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="2b39f-108">Cambiar el volumen de la reproducción de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="2b39f-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="2b39f-109">Windows proporciona las siguientes funciones para consultar y establecer el nivel de volumen de los dispositivos de salida de onda y audio.</span><span class="sxs-lookup"><span data-stu-id="2b39f-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="2b39f-110">Función</span><span class="sxs-lookup"><span data-stu-id="2b39f-110">Function</span></span>                                     | <span data-ttu-id="2b39f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b39f-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2b39f-112">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="2b39f-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="2b39f-113">Recupera el nivel de volumen actual del dispositivo de salida de forma de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="2b39f-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="2b39f-114">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="2b39f-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="2b39f-115">Establece el nivel de volumen del dispositivo de salida de onda-audio especificado.</span><span class="sxs-lookup"><span data-stu-id="2b39f-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="2b39f-116">No todos los dispositivos de audio de onda admiten cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="2b39f-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="2b39f-117">Algunos dispositivos admiten el control de volumen individual en los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="2b39f-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="2b39f-118">Para obtener información sobre cómo determinar las capacidades de control de volumen de los dispositivos de audio de forma de onda, consulte [dispositivos y tipos de datos](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="2b39f-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="2b39f-119">Algunas aplicaciones permiten al usuario controlar el volumen de todos los dispositivos de audio de un sistema.</span><span class="sxs-lookup"><span data-stu-id="2b39f-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="2b39f-120">(Muchas aplicaciones de este tipo usan los servicios de mezclador de audio; para obtener más información, consulte [mezcladores de audio](audio-mixers.md)). A menos que la aplicación sea capaz de realizar este tipo de control de volumen maestro, debe abrir un dispositivo de audio antes de cambiar su volumen.</span><span class="sxs-lookup"><span data-stu-id="2b39f-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="2b39f-121">También debe consultar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="2b39f-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="2b39f-122">El volumen se especifica en un valor de palabra.</span><span class="sxs-lookup"><span data-stu-id="2b39f-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="2b39f-123">Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="2b39f-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="2b39f-124">En el caso de los dispositivos que no admiten el control de volumen de canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="2b39f-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="2b39f-125">Los valores de nivel de volumen van desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente.</span><span class="sxs-lookup"><span data-stu-id="2b39f-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="2b39f-126">El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="2b39f-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 