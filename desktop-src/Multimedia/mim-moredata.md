---
title: MIM_MOREDATA mensaje (Mmsystem.h)
description: El mensaje MOREDATA de MIM se envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada DE MIDI recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE MIM lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de \_ \_ entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119419"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="4f214-104">Mensaje \_ MOREDATA de MIM</span><span class="sxs-lookup"><span data-stu-id="4f214-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="4f214-105">El **mensaje \_ MOREDATA** de MIM se envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada DE LÍNEA recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE [**\_ MIM**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f214-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="4f214-106">La función de devolución de llamada recibe este mensaje solo cuando la aplicación especifica EL ESTADO DE E/S de MIDI en la llamada \_ \_ a la función [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)</span><span class="sxs-lookup"><span data-stu-id="4f214-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="4f214-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f214-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f214-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="4f214-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="4f214-109">Especifica el mensaje MIDI que se recibió.</span><span class="sxs-lookup"><span data-stu-id="4f214-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="4f214-110">El mensaje se empaqueta en un **valor DWORD** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4f214-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="4f214-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f214-111">Requirement</span></span> | <span data-ttu-id="4f214-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4f214-112">Value</span></span> | <span data-ttu-id="4f214-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f214-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="4f214-114">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="4f214-114">High word</span></span> | <span data-ttu-id="4f214-115">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="4f214-115">High-order byte</span></span> | <span data-ttu-id="4f214-116">No se usa.</span><span class="sxs-lookup"><span data-stu-id="4f214-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="4f214-117">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="4f214-117">Low-order byte</span></span>  | <span data-ttu-id="4f214-118">Contiene un segundo byte de datos MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="4f214-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="4f214-119">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="4f214-119">Low word</span></span>  | <span data-ttu-id="4f214-120">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="4f214-120">High-order byte</span></span> | <span data-ttu-id="4f214-121">Contiene el primer byte de datos DE MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="4f214-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="4f214-122">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="4f214-122">Low-order byte</span></span>  | <span data-ttu-id="4f214-123">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f214-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="4f214-124">Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f214-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="4f214-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="4f214-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="4f214-126">Especifica la hora a la que el controlador de dispositivo de entrada recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f214-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="4f214-127">La marca de tiempo se especifica en milisegundos, empezando por 0 cuando se llamó a la [**función midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)</span><span class="sxs-lookup"><span data-stu-id="4f214-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f214-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f214-128">Return Value</span></span>

<span data-ttu-id="4f214-129">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="4f214-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f214-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f214-130">Remarks</span></span>

<span data-ttu-id="4f214-131">Una aplicación solo debe realizar una cantidad mínima de procesamiento de mensajes \_ MOREDATA de MIM.</span><span class="sxs-lookup"><span data-stu-id="4f214-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="4f214-132">(En concreto, las aplicaciones no deben llamar a la [función PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante el procesamiento de MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos del evento en un búfer y, a continuación, devolver.</span><span class="sxs-lookup"><span data-stu-id="4f214-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="4f214-133">Cuando una aplicación recibe un mensaje DE DATOS DE [**MIM \_**](mim-data.md) después de una serie de mensajes MOREDATA de MIM, se ha puesto al día con los eventos ENTRANTES DE MIDI y puede llamar de forma segura a funciones que consumen mucho \_ tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f214-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="4f214-134">Los mensajes MIDI recibidos de un puerto de entrada DE MIDI tienen deshabilitado el estado de ejecución; cada mensaje se expande para incluir el byte de estado DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f214-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="4f214-135">Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f214-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f214-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f214-136">Requirements</span></span>



| <span data-ttu-id="4f214-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f214-137">Requirement</span></span> | <span data-ttu-id="4f214-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4f214-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f214-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f214-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4f214-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4f214-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f214-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f214-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4f214-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f214-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f214-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f214-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f214-144"><dt>Mmsystem.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f214-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f214-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f214-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f214-146">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4f214-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4f214-147">Mensajes DE MIDI</span><span class="sxs-lookup"><span data-stu-id="4f214-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

