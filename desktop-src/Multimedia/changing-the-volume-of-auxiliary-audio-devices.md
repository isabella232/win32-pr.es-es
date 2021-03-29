---
title: Cambiar el volumen de Audio-Devices auxiliares
description: Cambiar el volumen de Audio-Devices auxiliares
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio de una onda, cambio del volumen del dispositivo de audio auxiliar
- cambiar el volumen del dispositivo de audio auxiliar
- audio auxiliar, cambio del volumen del dispositivo
- interfaz de audio auxiliar
- dispositivos de audio auxiliares, cambiar volumen
- audio auxiliar, interfaz
- audio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791638"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="5b4e2-110">Cambiar el volumen de Audio-Devices auxiliares</span><span class="sxs-lookup"><span data-stu-id="5b4e2-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="5b4e2-111">Windows proporciona las siguientes funciones para consultar y establecer el volumen de los dispositivos de audio auxiliares.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="5b4e2-112">Función</span><span class="sxs-lookup"><span data-stu-id="5b4e2-112">Function</span></span>                             | <span data-ttu-id="5b4e2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b4e2-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="5b4e2-114">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="5b4e2-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="5b4e2-115">Recupera la configuración del volumen actual del dispositivo de salida auxiliar especificado.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="5b4e2-116">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="5b4e2-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="5b4e2-117">Establece el volumen del dispositivo de salida auxiliar especificado.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="5b4e2-118">No todos los dispositivos de audio auxiliares admiten cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="5b4e2-119">Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="5b4e2-120">El volumen se especifica en un valor palabra, al igual que con las funciones de control de volumen de onda y audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="5b4e2-121">Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="5b4e2-122">En el caso de los dispositivos que no admiten el control de volumen de canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="5b4e2-123">Los valores de nivel de volumen van desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="5b4e2-124">El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 