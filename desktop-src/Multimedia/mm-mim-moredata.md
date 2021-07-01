---
title: MM_MIM_MOREDATA mensaje (Mmsystem.h)
description: El mensaje MM MIM MOREDATA se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE MIM lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de \_ \_ \_ entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120030"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="55519-104">Mensaje \_ MM MIM \_ MOREDATA</span><span class="sxs-lookup"><span data-stu-id="55519-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="55519-105">El **mensaje MM \_ MIM \_ MOREDATA** se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE [**MIM \_**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="55519-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="55519-106">La ventana recibe este mensaje solo cuando la aplicación especifica EL ESTADO DE E/S DE MIDI en \_ la llamada a la función \_ [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)</span><span class="sxs-lookup"><span data-stu-id="55519-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="55519-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55519-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55519-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="55519-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="55519-109">Controle el dispositivo de entrada de MIDI que recibió el mensaje DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="55519-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="55519-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="55519-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="55519-111">Especifica el mensaje MIDI que se recibió.</span><span class="sxs-lookup"><span data-stu-id="55519-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="55519-112">El mensaje se empaqueta en un valor doubleword como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="55519-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="55519-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="55519-113">Requirement</span></span> | <span data-ttu-id="55519-114">Valor</span><span class="sxs-lookup"><span data-stu-id="55519-114">Value</span></span> | <span data-ttu-id="55519-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="55519-115">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="55519-116">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="55519-116">High word</span></span> | <span data-ttu-id="55519-117">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="55519-117">High-order byte</span></span> | <span data-ttu-id="55519-118">No se usa.</span><span class="sxs-lookup"><span data-stu-id="55519-118">Not used.</span></span>                                           |
|           | <span data-ttu-id="55519-119">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="55519-119">Low-order byte</span></span>  | <span data-ttu-id="55519-120">Contiene un segundo byte de datos MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="55519-120">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="55519-121">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="55519-121">Low word</span></span>  | <span data-ttu-id="55519-122">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="55519-122">High-order byte</span></span> | <span data-ttu-id="55519-123">Contiene el primer byte de datos DE MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="55519-123">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="55519-124">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="55519-124">Low-order byte</span></span>  | <span data-ttu-id="55519-125">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="55519-125">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="55519-126">Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="55519-126">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55519-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55519-127">Return Value</span></span>

<span data-ttu-id="55519-128">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="55519-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55519-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55519-129">Remarks</span></span>

<span data-ttu-id="55519-130">Si la aplicación recibirá datos DE MIDI más rápido de lo que puede procesar, no debe usar un mecanismo de devolución de llamada de ventana.</span><span class="sxs-lookup"><span data-stu-id="55519-130">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="55519-131">Para maximizar la velocidad, use una función de devolución de llamada y use el mensaje [**\_ MOREDATA de MIM**](mim-moredata.md) en lugar de MM \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="55519-131">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="55519-132">Una aplicación solo debe realizar una cantidad mínima de procesamiento de mensajes \_ \_ MOREDATA de MM MIM.</span><span class="sxs-lookup"><span data-stu-id="55519-132">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="55519-133">(En concreto, las aplicaciones no deben llamar a la [función PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante el procesamiento de MM \_ MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos del evento en un búfer y, a continuación, devolver.</span><span class="sxs-lookup"><span data-stu-id="55519-133">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="55519-134">Cuando una aplicación recibe un mensaje [**MM \_ MIM \_ DATA**](mm-mim-data.md) después de una serie de mensajes \_ MM MIM MOREDATA, se ha puesto al día con los eventos ENTRANTES DE MIDI y puede llamar de forma segura a funciones que consumen mucho \_ tiempo.</span><span class="sxs-lookup"><span data-stu-id="55519-134">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="55519-135">Los mensajes DE MIDI recibidos desde un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="55519-135">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="55519-136">Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="55519-136">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="55519-137">No hay ninguna marca de tiempo disponible con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="55519-137">No time stamp is available with this message.</span></span> <span data-ttu-id="55519-138">Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="55519-138">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="55519-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55519-139">Requirements</span></span>



| <span data-ttu-id="55519-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="55519-140">Requirement</span></span> | <span data-ttu-id="55519-141">Valor</span><span class="sxs-lookup"><span data-stu-id="55519-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55519-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55519-142">Minimum supported client</span></span><br/> | <span data-ttu-id="55519-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55519-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="55519-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55519-144">Minimum supported server</span></span><br/> | <span data-ttu-id="55519-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55519-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="55519-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55519-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="55519-147"><dt>Mmsystem.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="55519-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55519-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="55519-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55519-149">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="55519-149">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="55519-150">Mensajes DE MIDI</span><span class="sxs-lookup"><span data-stu-id="55519-150">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

