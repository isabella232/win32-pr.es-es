---
title: Tipos de datos de salida MIDI
description: Tipos de datos de salida MIDI
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipos de datos de salida
- MIDI (interfaz digital de instrumentos musicales), tipos de datos de salida
- reproducir archivos MIDI, tipos de datos de salida
- Tipos de datos de salida MIDI
- MIDIHDR, tipo de datos
- MIDIOUTCAPS, tipo de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790894"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="a26a0-109">Tipos de datos de salida MIDI</span><span class="sxs-lookup"><span data-stu-id="a26a0-109">MIDI Output Data Types</span></span>

<span data-ttu-id="a26a0-110">Windows define los siguientes tipos de datos para las funciones de salida de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a26a0-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="a26a0-111">Value</span><span class="sxs-lookup"><span data-stu-id="a26a0-111">Value</span></span>                              | <span data-ttu-id="a26a0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="a26a0-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a26a0-113">**HMIDIOUT**</span><span class="sxs-lookup"><span data-stu-id="a26a0-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="a26a0-114">Identificador de un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="a26a0-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="a26a0-115">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="a26a0-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="a26a0-116">Encabezado para un bloque de datos exclusivos del sistema MIDI o de secuencia.</span><span class="sxs-lookup"><span data-stu-id="a26a0-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="a26a0-117">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="a26a0-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="a26a0-118">Estructura usada para consultar las capacidades de un dispositivo de salida MIDI determinado.</span><span class="sxs-lookup"><span data-stu-id="a26a0-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 