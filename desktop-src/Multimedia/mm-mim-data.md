---
title: MM_MIM_DATA mensaje (Mmsystem.h)
description: El mensaje MM MIM DATA se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje \_ \_ COMPLETO de MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119700"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="6ce35-104">Mensaje \_ MM MIM \_ DATA</span><span class="sxs-lookup"><span data-stu-id="6ce35-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="6ce35-105">El **mensaje \_ MM MIM \_ DATA** se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje COMPLETO de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="6ce35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ce35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce35-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6ce35-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6ce35-108">Controle el dispositivo de entrada de MIDI que recibió el mensaje DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="6ce35-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="6ce35-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="6ce35-110">Mensaje DE MIDI que se recibió.</span><span class="sxs-lookup"><span data-stu-id="6ce35-110">MIDI message that was received.</span></span> <span data-ttu-id="6ce35-111">El mensaje se empaqueta en un valor doubleword como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6ce35-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="6ce35-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ce35-112">Requirement</span></span> | <span data-ttu-id="6ce35-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6ce35-113">Value</span></span> | <span data-ttu-id="6ce35-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ce35-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="6ce35-115">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="6ce35-115">High word</span></span> | <span data-ttu-id="6ce35-116">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="6ce35-116">High-order byte</span></span> | <span data-ttu-id="6ce35-117">No se usa.</span><span class="sxs-lookup"><span data-stu-id="6ce35-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="6ce35-118">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="6ce35-118">Low-order byte</span></span>  | <span data-ttu-id="6ce35-119">Contiene un segundo byte de datos MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="6ce35-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="6ce35-120">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="6ce35-120">Low word</span></span>  | <span data-ttu-id="6ce35-121">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="6ce35-121">High-order byte</span></span> | <span data-ttu-id="6ce35-122">Contiene el primer byte de datos DE MIDI (cuando sea necesario).</span><span class="sxs-lookup"><span data-stu-id="6ce35-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="6ce35-123">Byte de orden bajo</span><span class="sxs-lookup"><span data-stu-id="6ce35-123">Low-order byte</span></span>  | <span data-ttu-id="6ce35-124">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="6ce35-125">Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce35-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ce35-126">Return Value</span></span>

<span data-ttu-id="6ce35-127">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="6ce35-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce35-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ce35-128">Remarks</span></span>

<span data-ttu-id="6ce35-129">Los mensajes DE MIDI recibidos desde un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="6ce35-130">Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="6ce35-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="6ce35-131">No hay ninguna marca de tiempo disponible con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="6ce35-131">No time stamp is available with this message.</span></span> <span data-ttu-id="6ce35-132">Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6ce35-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce35-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ce35-133">Requirements</span></span>



| <span data-ttu-id="6ce35-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ce35-134">Requirement</span></span> | <span data-ttu-id="6ce35-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6ce35-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce35-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ce35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6ce35-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ce35-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ce35-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ce35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6ce35-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ce35-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ce35-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ce35-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ce35-141"><dt>Mmsystem.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ce35-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ce35-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6ce35-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce35-143">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="6ce35-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6ce35-144">Mensajes DE MIDI</span><span class="sxs-lookup"><span data-stu-id="6ce35-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





