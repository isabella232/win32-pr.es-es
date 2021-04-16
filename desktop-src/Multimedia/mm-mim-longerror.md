---
title: Mensaje de MM_MIM_LONGERROR (mmsystem. h)
description: El \_ mensaje LONGERROR de MIM de mm \_ se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- Mensaje de MM_MIM_LONGERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686146"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="09ca1-104">Mensaje de LONGERROR de \_ MIM mm \_</span><span class="sxs-lookup"><span data-stu-id="09ca1-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="09ca1-105">El **mensaje \_ \_ LONGERROR de MIM de mm** se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.</span><span class="sxs-lookup"><span data-stu-id="09ca1-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="09ca1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ca1-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="09ca1-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="09ca1-108">Identificador del dispositivo de entrada MIDI que recibió el mensaje no válido.</span><span class="sxs-lookup"><span data-stu-id="09ca1-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="09ca1-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="09ca1-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="09ca1-110">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer que contiene el mensaje no válido.</span><span class="sxs-lookup"><span data-stu-id="09ca1-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ca1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09ca1-111">Return Value</span></span>

<span data-ttu-id="09ca1-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="09ca1-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09ca1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09ca1-113">Remarks</span></span>

<span data-ttu-id="09ca1-114">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="09ca1-114">The returned buffer might not be full.</span></span> <span data-ttu-id="09ca1-115">Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="09ca1-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ca1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09ca1-116">Requirements</span></span>



| <span data-ttu-id="09ca1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ca1-117">Requirement</span></span> | <span data-ttu-id="09ca1-118">Value</span><span class="sxs-lookup"><span data-stu-id="09ca1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ca1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09ca1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09ca1-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09ca1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09ca1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09ca1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09ca1-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09ca1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09ca1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09ca1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ca1-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09ca1-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ca1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="09ca1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ca1-126">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="09ca1-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="09ca1-127">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="09ca1-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

