---
title: Waveform-Audio tipos de datos de entrada
description: Waveform-Audio tipos de datos de entrada
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio de la onda, tipos de datos de entrada
- 'onda: interfaz de audio, tipos de datos de entrada'
- grabar audio de onda, tipos de datos de entrada
- Identificador de HWAVEIN
- WAVEFORMATEX (estructura)
- Estructura WAVEHDR
- Estructura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077683"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="26fba-110">Waveform-Audio tipos de datos de entrada</span><span class="sxs-lookup"><span data-stu-id="26fba-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="26fba-111">Los siguientes tipos de datos se definen para las funciones de entrada de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="26fba-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="26fba-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="26fba-112">Type</span></span>                                 | <span data-ttu-id="26fba-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="26fba-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fba-114">**HWAVEIN**</span><span class="sxs-lookup"><span data-stu-id="26fba-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="26fba-115">Identificador de un dispositivo de entrada de audio de onda abierta.</span><span class="sxs-lookup"><span data-stu-id="26fba-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="26fba-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="26fba-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="26fba-117">Estructura que especifica los formatos de datos admitidos por un dispositivo de entrada de audio de forma de onda determinado.</span><span class="sxs-lookup"><span data-stu-id="26fba-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="26fba-118">Esta estructura también se utiliza para los dispositivos de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="26fba-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="26fba-119">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="26fba-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="26fba-120">Estructura utilizada como encabezado para un bloque de datos de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="26fba-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="26fba-121">Esta estructura también se utiliza para los dispositivos de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="26fba-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="26fba-122">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="26fba-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="26fba-123">Estructura usada para consultar las capacidades de un dispositivo de entrada de audio de forma de onda determinado.</span><span class="sxs-lookup"><span data-stu-id="26fba-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="26fba-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26fba-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26fba-125">Grabación de audio de onda</span><span class="sxs-lookup"><span data-stu-id="26fba-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 