---
title: Mensaje de MIM_MOREDATA (mmsystem. h)
description: El mensaje de MOREDATA de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando \_ los mensajes de datos de MIM lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Mensaje de MIM_MOREDATA de Windows multimedia
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
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804099"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="cea1c-104">Mensaje de MOREDATA de MIM \_</span><span class="sxs-lookup"><span data-stu-id="cea1c-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="cea1c-105">El mensaje de **\_ MOREDATA de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cea1c-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="cea1c-106">La función de devolución de llamada recibe este mensaje solo cuando la aplicación especifica el \_ Estado de e/s \_ de MIDI en la llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="cea1c-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="cea1c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cea1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea1c-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="cea1c-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="cea1c-109">Especifica el mensaje MIDI recibido.</span><span class="sxs-lookup"><span data-stu-id="cea1c-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="cea1c-110">El mensaje se empaqueta en un valor **DWORD** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cea1c-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="cea1c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea1c-111">Requirement</span></span> | <span data-ttu-id="cea1c-112">Value</span><span class="sxs-lookup"><span data-stu-id="cea1c-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="cea1c-113">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="cea1c-113">High word</span></span> | <span data-ttu-id="cea1c-114">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="cea1c-114">High-order byte</span></span> | <span data-ttu-id="cea1c-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cea1c-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="cea1c-116">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="cea1c-116">Low-order byte</span></span>  | <span data-ttu-id="cea1c-117">Contiene un segundo byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="cea1c-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="cea1c-118">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="cea1c-118">Low word</span></span>  | <span data-ttu-id="cea1c-119">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="cea1c-119">High-order byte</span></span> | <span data-ttu-id="cea1c-120">Contiene el primer byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="cea1c-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="cea1c-121">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="cea1c-121">Low-order byte</span></span>  | <span data-ttu-id="cea1c-122">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cea1c-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="cea1c-123">Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cea1c-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="cea1c-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="cea1c-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="cea1c-125">Especifica la hora a la que el controlador de dispositivo de entrada recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cea1c-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="cea1c-126">La marca de tiempo se especifica en milisegundos, empezando en 0 cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="cea1c-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea1c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cea1c-127">Return Value</span></span>

<span data-ttu-id="cea1c-128">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cea1c-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea1c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cea1c-129">Remarks</span></span>

<span data-ttu-id="cea1c-130">Una aplicación solo debe realizar una cantidad mínima de procesamiento de \_ mensajes MOREDATA de MIM.</span><span class="sxs-lookup"><span data-stu-id="cea1c-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="cea1c-131">(En concreto, las aplicaciones no deben llamar a la función [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) mientras PROCESAn MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos de evento en un búfer y, a continuación, devolver.</span><span class="sxs-lookup"><span data-stu-id="cea1c-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="cea1c-132">Cuando una aplicación recibe un mensaje de [**\_ datos de MIM**](mim-data.md) después de una serie de mensajes de MOREDATA de MIM, se ha puesto al \_ día con los eventos MIDI entrantes y puede llamar a funciones con un uso intensivo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="cea1c-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="cea1c-133">Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cea1c-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="cea1c-134">No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="cea1c-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea1c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea1c-135">Requirements</span></span>



| <span data-ttu-id="cea1c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea1c-136">Requirement</span></span> | <span data-ttu-id="cea1c-137">Value</span><span class="sxs-lookup"><span data-stu-id="cea1c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea1c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea1c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cea1c-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cea1c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cea1c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea1c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cea1c-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cea1c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cea1c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cea1c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea1c-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cea1c-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea1c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea1c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea1c-145">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="cea1c-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="cea1c-146">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="cea1c-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

