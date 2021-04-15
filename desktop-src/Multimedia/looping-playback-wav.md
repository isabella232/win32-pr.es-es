---
title: Reproducción en bucle (audio de onda)
description: Reproducción en bucle (audio de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio de una onda, sonidos en bucle
- 'onda: interfaz de audio, sonidos en bucle'
- audio de una onda, reproducción en bucle
- 'onda: interfaz de audio, reproducción en bucle'
- 'onda de onda de bucle: sonidos de audio'
- 'onda en bucle: reproducción de audio'
- waveOutWrite función)
- waveOutBreakLoop función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105654027"
---
# <a name="looping-playback"></a><span data-ttu-id="0d1d8-111">Reproducción en bucle</span><span class="sxs-lookup"><span data-stu-id="0d1d8-111">Looping Playback</span></span>

<span data-ttu-id="0d1d8-112">El bucle de un sonido lo controlan los miembros **dwLoops** y **dwFlags** en las estructuras [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que se pasan al dispositivo con la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="0d1d8-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="0d1d8-113">Use las marcas **WHDR \_ BEGINLOOP** y **WHDR \_ ENDLOOP** en el miembro **dwFlags** para especificar los bloques de datos inicial y final para el bucle.</span><span class="sxs-lookup"><span data-stu-id="0d1d8-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="0d1d8-114">Para recorrer un solo bloque de datos, especifique ambos marcadores para el mismo bloque.</span><span class="sxs-lookup"><span data-stu-id="0d1d8-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="0d1d8-115">Para especificar el número de bucles, utilice el miembro **dwLoops** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para el primer bloque del bucle.</span><span class="sxs-lookup"><span data-stu-id="0d1d8-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="0d1d8-116">Puede llamar a la función [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para detener un sonido de bucle.</span><span class="sxs-lookup"><span data-stu-id="0d1d8-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d1d8-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d1d8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1d8-118">Reproducir archivos Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="0d1d8-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
