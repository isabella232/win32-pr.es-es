---
title: Mensaje de MM_MIM_LONGDATA (mmsystem. h)
description: El mensaje de LONGDATA de MIM de MM \_ \_ se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- Mensaje de MM_MIM_LONGDATA de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151027"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="33c26-104">Mensaje de LONGDATA de \_ MIM mm \_</span><span class="sxs-lookup"><span data-stu-id="33c26-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="33c26-105">El mensaje de **\_ \_ LONGDATA de MIM de mm** se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="33c26-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="33c26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c26-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="33c26-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="33c26-108">Identificador del dispositivo de entrada MIDI que recibió los datos.</span><span class="sxs-lookup"><span data-stu-id="33c26-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="33c26-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="33c26-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="33c26-110">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="33c26-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c26-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33c26-111">Return Value</span></span>

<span data-ttu-id="33c26-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="33c26-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c26-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33c26-113">Remarks</span></span>

<span data-ttu-id="33c26-114">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="33c26-114">The returned buffer might not be full.</span></span> <span data-ttu-id="33c26-115">Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a la que apunta *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="33c26-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="33c26-116">No hay ninguna marca de tiempo disponible con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="33c26-116">No time stamp is available with this message.</span></span> <span data-ttu-id="33c26-117">En el caso de los datos de entrada con marca de tiempo, debe utilizar los mensajes que se envían a las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="33c26-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c26-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c26-118">Requirements</span></span>



| <span data-ttu-id="33c26-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c26-119">Requirement</span></span> | <span data-ttu-id="33c26-120">Value</span><span class="sxs-lookup"><span data-stu-id="33c26-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c26-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33c26-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33c26-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="33c26-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="33c26-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33c26-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33c26-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33c26-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33c26-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33c26-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c26-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33c26-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c26-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c26-128">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="33c26-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="33c26-129">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="33c26-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

