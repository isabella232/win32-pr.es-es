---
title: Mensaje de MIM_ERROR (mmsystem. h)
description: El mensaje de error de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando se recibe un mensaje MIDI no válido.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- Mensaje de MIM_ERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149975"
---
# <a name="mim_error-message"></a><span data-ttu-id="a18ff-104">Mensaje de error de MIM \_</span><span class="sxs-lookup"><span data-stu-id="a18ff-104">MIM\_ERROR message</span></span>

<span data-ttu-id="a18ff-105">El mensaje de **\_ error de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando se recibe un mensaje MIDI no válido.</span><span class="sxs-lookup"><span data-stu-id="a18ff-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="a18ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a18ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a18ff-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="a18ff-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="a18ff-108">Mensaje MIDI no válido que se recibió.</span><span class="sxs-lookup"><span data-stu-id="a18ff-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="a18ff-109">El mensaje se empaqueta en un valor palabra con el primer byte del mensaje en el byte de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="a18ff-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="a18ff-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="a18ff-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="a18ff-111">Hora en que el controlador del dispositivo de entrada recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a18ff-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="a18ff-112">La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="a18ff-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a18ff-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a18ff-113">Return Value</span></span>

<span data-ttu-id="a18ff-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a18ff-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a18ff-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a18ff-115">Requirements</span></span>



| <span data-ttu-id="a18ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a18ff-116">Requirement</span></span> | <span data-ttu-id="a18ff-117">Value</span><span class="sxs-lookup"><span data-stu-id="a18ff-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18ff-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a18ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a18ff-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a18ff-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a18ff-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a18ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a18ff-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a18ff-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a18ff-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a18ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a18ff-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a18ff-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a18ff-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a18ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18ff-125">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="a18ff-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a18ff-126">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="a18ff-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

