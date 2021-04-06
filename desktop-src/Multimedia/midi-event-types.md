---
title: Tipos de eventos MIDI
description: Tipos de eventos MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipos de evento
- MIDI (interfaz digital de instrumentos musicales), tipos de evento
- Estructura MIDIEVENT
- búferes de secuencia, tipos de eventos MIDI
- Tipos de eventos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077731"
---
# <a name="midi-event-types"></a><span data-ttu-id="2b551-108">Tipos de eventos MIDI</span><span class="sxs-lookup"><span data-stu-id="2b551-108">MIDI Event Types</span></span>

<span data-ttu-id="2b551-109">El miembro **dwEvent** de la estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) describe el evento MIDI que debe tener lugar.</span><span class="sxs-lookup"><span data-stu-id="2b551-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="2b551-110">Los eventos cortos solo se ajustan a este miembro.</span><span class="sxs-lookup"><span data-stu-id="2b551-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="2b551-111">Los eventos Long requieren uno o varios valores de palabra además del miembro **dwEvent** para almacenar las descripciones de evento.</span><span class="sxs-lookup"><span data-stu-id="2b551-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="2b551-112">El byte alto del miembro **dwEvent** contiene información sobre si el evento es largo o corto y sobre si se genera una devolución de llamada junto con el evento.</span><span class="sxs-lookup"><span data-stu-id="2b551-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="2b551-113">Además, este byte se utiliza para describir el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="2b551-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="2b551-114">Los 24 bits restantes del miembro **dwEvent** se usan para contener los parámetros de evento (para mensajes cortos) o para contener la longitud de los parámetros de evento (para los mensajes largos).</span><span class="sxs-lookup"><span data-stu-id="2b551-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="2b551-115">Para extraer información del miembro **dwEvent** , use las macros [**MEVT \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) y [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .</span><span class="sxs-lookup"><span data-stu-id="2b551-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="2b551-116">Para obtener una descripción de los tipos de eventos predefinidos, consulte el material de referencia de la estructura **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="2b551-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 