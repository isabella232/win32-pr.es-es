---
title: MIM_DATA mensaje (Mmsystem.h)
description: El mensaje MIM DATA se envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada MIDI recibe un \_ mensaje MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA mensaje multimedia de Windows
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118410"
---
# <a name="mim_data-message"></a><span data-ttu-id="16c8b-104">Mensaje DE \_ DATOS DE MIM</span><span class="sxs-lookup"><span data-stu-id="16c8b-104">MIM\_DATA message</span></span>

<span data-ttu-id="16c8b-105">El **mensaje MIM \_ DATA se** envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada DE LÍNEA recibe un mensaje DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="16c8b-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="16c8b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16c8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c8b-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="16c8b-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="16c8b-108">Mensaje DE MIDI que se recibió.</span><span class="sxs-lookup"><span data-stu-id="16c8b-108">MIDI message that was received.</span></span> <span data-ttu-id="16c8b-109">El mensaje se empaqueta en un valor doubleword como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="16c8b-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="16c8b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c8b-110">Requirement</span></span> | <span data-ttu-id="16c8b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="16c8b-111">Value</span></span> | <span data-ttu-id="16c8b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="16c8b-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="16c8b-113">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="16c8b-113">High word</span></span> | <span data-ttu-id="16c8b-114">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="16c8b-114">High-order byte</span></span> | <span data-ttu-id="16c8b-115">No se usa.</span><span class="sxs-lookup"><span data-stu-id="16c8b-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="16c8b-116">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="16c8b-116">Low-order byte</span></span>  | <span data-ttu-id="16c8b-117">Contiene un segundo byte de datos DE MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="16c8b-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="16c8b-118">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="16c8b-118">Low word</span></span>  | <span data-ttu-id="16c8b-119">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="16c8b-119">High-order byte</span></span> | <span data-ttu-id="16c8b-120">Contiene el primer byte de datos DE MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="16c8b-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="16c8b-121">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="16c8b-121">Low-order byte</span></span>  | <span data-ttu-id="16c8b-122">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="16c8b-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="16c8b-123">Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="16c8b-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="16c8b-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="16c8b-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="16c8b-125">Hora a la que el controlador de dispositivo de entrada recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="16c8b-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="16c8b-126">La marca de tiempo se especifica en milisegundos, empezando en cero cuando se llamó [**a la función midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)</span><span class="sxs-lookup"><span data-stu-id="16c8b-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c8b-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16c8b-127">Return Value</span></span>

<span data-ttu-id="16c8b-128">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="16c8b-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c8b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16c8b-129">Remarks</span></span>

<span data-ttu-id="16c8b-130">Los mensajes DE MIDI recibidos de un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="16c8b-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="16c8b-131">Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="16c8b-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c8b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c8b-132">Requirements</span></span>



| <span data-ttu-id="16c8b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c8b-133">Requirement</span></span> | <span data-ttu-id="16c8b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="16c8b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c8b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c8b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="16c8b-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="16c8b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="16c8b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c8b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="16c8b-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16c8b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="16c8b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16c8b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="16c8b-140"><dt>Mmsystem.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="16c8b-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c8b-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16c8b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c8b-142">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="16c8b-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="16c8b-143">Mensajes DE MIDI</span><span class="sxs-lookup"><span data-stu-id="16c8b-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

