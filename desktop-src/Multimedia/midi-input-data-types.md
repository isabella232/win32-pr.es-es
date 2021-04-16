---
title: Tipos de datos de entrada MIDI
description: Tipos de datos de entrada MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipos de datos de entrada
- MIDI (interfaz digital de instrumentos musicales), tipos de datos de entrada
- grabar audio MIDI, tipos de datos de entrada
- Tipos de datos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676373"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="f9dc5-107">Tipos de datos de entrada MIDI</span><span class="sxs-lookup"><span data-stu-id="f9dc5-107">MIDI Input Data Types</span></span>

<span data-ttu-id="f9dc5-108">Windows define los siguientes tipos de datos para las funciones de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f9dc5-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="f9dc5-109">Value</span><span class="sxs-lookup"><span data-stu-id="f9dc5-109">Value</span></span>                            | <span data-ttu-id="f9dc5-110">Significado</span><span class="sxs-lookup"><span data-stu-id="f9dc5-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dc5-111">**HMIDIIN**</span><span class="sxs-lookup"><span data-stu-id="f9dc5-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="f9dc5-112">Identificador de un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f9dc5-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="f9dc5-113">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="f9dc5-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="f9dc5-114">Encabezado para un búfer de secuencia o un bloque de datos exclusivos del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="f9dc5-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="f9dc5-115">En el caso de las aplicaciones de entrada, esta estructura solo registra los datos exclusivos del sistema (no se admite la transmisión por secuencias para la entrada MIDI).</span><span class="sxs-lookup"><span data-stu-id="f9dc5-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="f9dc5-116">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="f9dc5-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="f9dc5-117">Estructura usada para consultar las capacidades de un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f9dc5-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="f9dc5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9dc5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9dc5-119">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="f9dc5-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 