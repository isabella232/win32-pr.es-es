---
title: Mensaje de MIM_DATA (mmsystem. h)
description: El mensaje de datos de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- Mensaje de MIM_DATA de Windows multimedia
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
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905659"
---
# <a name="mim_data-message"></a><span data-ttu-id="8be7c-104">Mensaje de datos de MIM \_</span><span class="sxs-lookup"><span data-stu-id="8be7c-104">MIM\_DATA message</span></span>

<span data-ttu-id="8be7c-105">El mensaje de **\_ datos de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI.</span><span class="sxs-lookup"><span data-stu-id="8be7c-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="8be7c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8be7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be7c-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="8be7c-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="8be7c-108">Mensaje MIDI recibido.</span><span class="sxs-lookup"><span data-stu-id="8be7c-108">MIDI message that was received.</span></span> <span data-ttu-id="8be7c-109">El mensaje se empaqueta en un valor de palabra como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8be7c-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="8be7c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be7c-110">Requirement</span></span> | <span data-ttu-id="8be7c-111">Value</span><span class="sxs-lookup"><span data-stu-id="8be7c-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="8be7c-112">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="8be7c-112">High word</span></span> | <span data-ttu-id="8be7c-113">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="8be7c-113">High-order byte</span></span> | <span data-ttu-id="8be7c-114">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8be7c-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="8be7c-115">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="8be7c-115">Low-order byte</span></span>  | <span data-ttu-id="8be7c-116">Contiene un segundo byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="8be7c-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="8be7c-117">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="8be7c-117">Low word</span></span>  | <span data-ttu-id="8be7c-118">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="8be7c-118">High-order byte</span></span> | <span data-ttu-id="8be7c-119">Contiene el primer byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="8be7c-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="8be7c-120">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="8be7c-120">Low-order byte</span></span>  | <span data-ttu-id="8be7c-121">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8be7c-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="8be7c-122">Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8be7c-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="8be7c-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="8be7c-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="8be7c-124">Hora en que el controlador del dispositivo de entrada recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8be7c-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="8be7c-125">La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="8be7c-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be7c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8be7c-126">Return Value</span></span>

<span data-ttu-id="8be7c-127">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8be7c-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be7c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8be7c-128">Remarks</span></span>

<span data-ttu-id="8be7c-129">Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8be7c-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="8be7c-130">No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8be7c-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be7c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be7c-131">Requirements</span></span>



| <span data-ttu-id="8be7c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be7c-132">Requirement</span></span> | <span data-ttu-id="8be7c-133">Value</span><span class="sxs-lookup"><span data-stu-id="8be7c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be7c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8be7c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8be7c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8be7c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8be7c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8be7c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8be7c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8be7c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8be7c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8be7c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be7c-139"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8be7c-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be7c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8be7c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be7c-141">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="8be7c-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8be7c-142">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="8be7c-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

