---
title: Mensaje de MM_MIM_DATA (mmsystem. h)
description: El \_ mensaje de datos de MIM mm \_ se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje MIDI completo.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- Mensaje de MM_MIM_DATA de Windows multimedia
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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078977"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="2f2b7-104">Mensaje de datos de MM \_ MIM \_</span><span class="sxs-lookup"><span data-stu-id="2f2b7-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="2f2b7-105">El mensaje de **\_ \_ datos de MIM mm** se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje MIDI completo.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="2f2b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f2b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2b7-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="2f2b7-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="2f2b7-108">Identificador del dispositivo de entrada MIDI que recibió el mensaje MIDI.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="2f2b7-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="2f2b7-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="2f2b7-110">Mensaje MIDI recibido.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-110">MIDI message that was received.</span></span> <span data-ttu-id="2f2b7-111">El mensaje se empaqueta en un valor de palabra como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2f2b7-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="2f2b7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2b7-112">Requirement</span></span> | <span data-ttu-id="2f2b7-113">Value</span><span class="sxs-lookup"><span data-stu-id="2f2b7-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="2f2b7-114">Palabra alta</span><span class="sxs-lookup"><span data-stu-id="2f2b7-114">High word</span></span> | <span data-ttu-id="2f2b7-115">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="2f2b7-115">High-order byte</span></span> | <span data-ttu-id="2f2b7-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="2f2b7-117">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="2f2b7-117">Low-order byte</span></span>  | <span data-ttu-id="2f2b7-118">Contiene un segundo byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="2f2b7-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="2f2b7-119">Palabra baja</span><span class="sxs-lookup"><span data-stu-id="2f2b7-119">Low word</span></span>  | <span data-ttu-id="2f2b7-120">Byte de orden superior</span><span class="sxs-lookup"><span data-stu-id="2f2b7-120">High-order byte</span></span> | <span data-ttu-id="2f2b7-121">Contiene el primer byte de datos MIDI (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="2f2b7-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="2f2b7-122">Byte de orden inferior</span><span class="sxs-lookup"><span data-stu-id="2f2b7-122">Low-order byte</span></span>  | <span data-ttu-id="2f2b7-123">Contiene el estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="2f2b7-124">Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2b7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f2b7-125">Return Value</span></span>

<span data-ttu-id="2f2b7-126">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2b7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f2b7-127">Remarks</span></span>

<span data-ttu-id="2f2b7-128">Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="2f2b7-129">No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="2f2b7-130">No hay ninguna marca de tiempo disponible con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-130">No time stamp is available with this message.</span></span> <span data-ttu-id="2f2b7-131">En el caso de los datos de entrada con marca de tiempo, debe utilizar los mensajes que se envían a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2f2b7-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2b7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f2b7-132">Requirements</span></span>



| <span data-ttu-id="2f2b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2b7-133">Requirement</span></span> | <span data-ttu-id="2f2b7-134">Value</span><span class="sxs-lookup"><span data-stu-id="2f2b7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2b7-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f2b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2b7-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f2b7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f2b7-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f2b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2b7-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f2b7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f2b7-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f2b7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f2b7-140"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f2b7-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2b7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f2b7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2b7-142">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="2f2b7-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="2f2b7-143">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="2f2b7-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





