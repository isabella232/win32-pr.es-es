---
title: Flujos MIDI
description: Flujos MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Interfaz digital de instrumentos musicales (MIDI), secuencias
- MIDI (interfaz digital de instrumentos musicales), secuencias
- búferes de secuencia, flujos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149251"
---
# <a name="midi-streams"></a><span data-ttu-id="f6f8f-106">Flujos MIDI</span><span class="sxs-lookup"><span data-stu-id="f6f8f-106">MIDI Streams</span></span>

<span data-ttu-id="f6f8f-107">Los eventos MIDI se producen en el contexto de un flujo de datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="f6f8f-108">Aunque una aplicación puede utilizar varias secuencias para definir datos musicales, el asignador MIDI no reconoce varias secuencias.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="f6f8f-109">La mayoría de las aplicaciones que usan secuencias usan una sola secuencia MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="f6f8f-110">Las siguientes funciones de funcionan con secuencias.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-110">The following functions work with streams.</span></span>



| <span data-ttu-id="f6f8f-111">Value</span><span class="sxs-lookup"><span data-stu-id="f6f8f-111">Value</span></span>                                            | <span data-ttu-id="f6f8f-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f6f8f-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="f6f8f-113">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="f6f8f-114">Cierra una secuencia MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="f6f8f-115">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="f6f8f-116">Abre un flujo MIDI y recupera un identificador.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="f6f8f-117">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="f6f8f-118">Reproduce o pone en cola un flujo (búfer) de datos MIDI en un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="f6f8f-119">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="f6f8f-120">Pausa la reproducción de una secuencia MIDI especificada.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="f6f8f-121">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="f6f8f-122">Recupera la posición actual en una secuencia MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="f6f8f-123">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="f6f8f-124">Establece y recupera las propiedades de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="f6f8f-125">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="f6f8f-126">Reinicia la reproducción de una secuencia MIDI en pausa.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="f6f8f-127">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="f6f8f-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="f6f8f-128">Desactiva todas las notas en todos los canales MIDI de la secuencia MIDI especificada.</span><span class="sxs-lookup"><span data-stu-id="f6f8f-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 