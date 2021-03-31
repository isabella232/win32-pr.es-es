---
title: Mensaje de MM_MIM_MOREDATA (mmsystem. h)
description: El mensaje de MOREDATA de MIM de MM \_ \_ se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando \_ los mensajes de datos de MIM lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- Mensaje de MM_MIM_MOREDATA de Windows multimedia
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
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079345"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="cbc22-104">Mensaje de MOREDATA de \_ MIM mm \_</span><span class="sxs-lookup"><span data-stu-id="cbc22-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="cbc22-105">El mensaje de **\_ \_ MOREDATA de MIM de mm** se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cbc22-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="cbc22-106">La ventana recibe este mensaje solo cuando la aplicación especifica el \_ Estado de e/s \_ de MIDI en la llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="cbc22-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="cbc22-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbc22-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc22-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="cbc22-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="cbc22-109">Identificador del dispositivo de entrada MIDI que recibió el mensaje MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbc22-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="cbc22-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="cbc22-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="cbc22-111">Especifica el mensaje MIDI recibido.</span><span class="sxs-lookup"><span data-stu-id="cbc22-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="cbc22-112">El mensaje se empaqueta en un valor de palabra como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cbc22-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="cbc22-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc22-113">Requirement</span></span> | <span data-ttu-id="cbc22-114">Value</span><span class="sxs-lookup"><span data-stu-id="cbc22-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="cbc22-115">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="cbc22-115">High word</span></span> | <span data-ttu-id="cbc22-116">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="cbc22-116">High-order byte</span></span> | <span data-ttu-id="cbc22-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cbc22-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="cbc22-118">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="cbc22-118">Low-order byte</span></span>  | <span data-ttu-id="cbc22-119">Contiene un segundo byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="cbc22-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="cbc22-120">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="cbc22-120">Low word</span></span>  | <span data-ttu-id="cbc22-121">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="cbc22-121">High-order byte</span></span> | <span data-ttu-id="cbc22-122">Contiene el primer byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="cbc22-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="cbc22-123">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="cbc22-123">Low-order byte</span></span>  | <span data-ttu-id="cbc22-124">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbc22-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="cbc22-125">Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbc22-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc22-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbc22-126">Return Value</span></span>

<span data-ttu-id="cbc22-127">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cbc22-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc22-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbc22-128">Remarks</span></span>

<span data-ttu-id="cbc22-129">Si la aplicación va a recibir datos MIDI más rápido de lo que puede procesarlos, no debe utilizar un mecanismo de devolución de llamada de ventana.</span><span class="sxs-lookup"><span data-stu-id="cbc22-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="cbc22-130">Para maximizar la velocidad, use una función de devolución de llamada y use el mensaje de [**\_ MOREDATA de MIM**](mim-moredata.md) en lugar de mm \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="cbc22-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="cbc22-131">Una aplicación solo debe realizar una cantidad mínima de procesamiento de mensajes de MOREDATA de MIM de MM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbc22-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="cbc22-132">(En particular, las aplicaciones no deben llamar a la función [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) mientras PROCESAn mm \_ MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos de evento en un búfer y, a continuación, devolver.</span><span class="sxs-lookup"><span data-stu-id="cbc22-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="cbc22-133">Cuando una aplicación recibe un mensaje de [**\_ \_ datos de mm MIM**](mm-mim-data.md) después de una serie de mensajes de MOREDATA de MIM de mm, se ha puesto al \_ \_ día con los eventos MIDI entrantes y puede llamar a funciones que consumen mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="cbc22-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="cbc22-134">Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbc22-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="cbc22-135">No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbc22-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="cbc22-136">No hay ninguna marca de tiempo disponible con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbc22-136">No time stamp is available with this message.</span></span> <span data-ttu-id="cbc22-137">En el caso de los datos de entrada con marca de tiempo, debe utilizar los mensajes que se envían a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cbc22-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc22-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc22-138">Requirements</span></span>



| <span data-ttu-id="cbc22-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc22-139">Requirement</span></span> | <span data-ttu-id="cbc22-140">Value</span><span class="sxs-lookup"><span data-stu-id="cbc22-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc22-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbc22-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc22-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cbc22-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cbc22-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbc22-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc22-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbc22-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cbc22-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbc22-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc22-146"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc22-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc22-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbc22-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc22-148">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="cbc22-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="cbc22-149">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="cbc22-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

