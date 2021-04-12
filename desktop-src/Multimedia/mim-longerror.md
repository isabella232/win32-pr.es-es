---
title: Mensaje de MIM_LONGERROR (mmsystem. h)
description: El mensaje de LONGERROR de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- Mensaje de MIM_LONGERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489401"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="6a565-104">Mensaje de LONGERROR de MIM \_</span><span class="sxs-lookup"><span data-stu-id="6a565-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="6a565-105">El mensaje de **\_ LONGERROR de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.</span><span class="sxs-lookup"><span data-stu-id="6a565-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="6a565-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a565-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="6a565-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="6a565-108">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer que contiene el mensaje no válido.</span><span class="sxs-lookup"><span data-stu-id="6a565-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="6a565-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="6a565-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="6a565-110">Hora a la que el controlador del dispositivo de entrada recibió los datos.</span><span class="sxs-lookup"><span data-stu-id="6a565-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="6a565-111">La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="6a565-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a565-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a565-112">Return Value</span></span>

<span data-ttu-id="6a565-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6a565-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a565-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a565-114">Remarks</span></span>

<span data-ttu-id="6a565-115">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="6a565-115">The returned buffer might not be full.</span></span> <span data-ttu-id="6a565-116">Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="6a565-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a565-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a565-117">Requirements</span></span>



| <span data-ttu-id="6a565-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a565-118">Requirement</span></span> | <span data-ttu-id="6a565-119">Value</span><span class="sxs-lookup"><span data-stu-id="6a565-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a565-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a565-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a565-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6a565-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6a565-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a565-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a565-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a565-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6a565-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a565-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a565-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a565-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a565-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a565-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a565-127">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="6a565-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6a565-128">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="6a565-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

