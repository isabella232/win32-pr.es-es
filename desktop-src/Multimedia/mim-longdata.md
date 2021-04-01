---
title: Mensaje de MIM_LONGDATA (mmsystem. h)
description: El mensaje de LONGDATA de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve a la aplicación.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- Mensaje de MIM_LONGDATA de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151235"
---
# <a name="mim_longdata-message"></a><span data-ttu-id="d01b6-104">Mensaje de LONGDATA de MIM \_</span><span class="sxs-lookup"><span data-stu-id="d01b6-104">MIM\_LONGDATA message</span></span>

<span data-ttu-id="d01b6-105">El mensaje de **\_ LONGDATA de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d01b6-105">The **MIM\_LONGDATA** message is sent to a MIDI input callback function when a system-exclusive buffer has been filled with data and is being returned to the application.</span></span>


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="d01b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d01b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d01b6-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="d01b6-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="d01b6-108">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="d01b6-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d01b6-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="d01b6-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="d01b6-110">Hora a la que el controlador del dispositivo de entrada recibió los datos.</span><span class="sxs-lookup"><span data-stu-id="d01b6-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="d01b6-111">La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="d01b6-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d01b6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d01b6-112">Return Value</span></span>

<span data-ttu-id="d01b6-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d01b6-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01b6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d01b6-114">Remarks</span></span>

<span data-ttu-id="d01b6-115">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="d01b6-115">The returned buffer might not be full.</span></span> <span data-ttu-id="d01b6-116">Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="d01b6-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01b6-117">Requirements</span></span>



| <span data-ttu-id="d01b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01b6-118">Requirement</span></span> | <span data-ttu-id="d01b6-119">Value</span><span class="sxs-lookup"><span data-stu-id="d01b6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01b6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d01b6-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d01b6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d01b6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d01b6-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d01b6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d01b6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d01b6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d01b6-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d01b6-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01b6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d01b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01b6-127">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="d01b6-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="d01b6-128">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="d01b6-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

