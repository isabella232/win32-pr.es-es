---
title: Mensaje de MM_MOM_POSITIONCB (mmsystem. h)
description: El \_ mensaje POSITIONCB de MOM de mm \_ se envía a una ventana cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- Mensaje de MM_MOM_POSITIONCB de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995995"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="239e3-104">Mensaje de POSITIONCB de \_ MOM de mm \_</span><span class="sxs-lookup"><span data-stu-id="239e3-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="239e3-105">El **mensaje \_ \_ POSITIONCB de MOM de mm** se envía a una ventana cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.</span><span class="sxs-lookup"><span data-stu-id="239e3-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="239e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="239e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239e3-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="239e3-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="239e3-108">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el evento que provocó la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="239e3-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="239e3-109">El miembro **dwOffset** proporciona el desplazamiento del evento.</span><span class="sxs-lookup"><span data-stu-id="239e3-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="239e3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="239e3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="239e3-111">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="239e3-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239e3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="239e3-112">Return Value</span></span>

<span data-ttu-id="239e3-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="239e3-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="239e3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="239e3-114">Remarks</span></span>

<span data-ttu-id="239e3-115">La reproducción del búfer de secuencia continúa incluso mientras se ejecuta la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="239e3-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="239e3-116">Todos los eventos después del \_ \_ evento de devolución de llamada de MEVT F en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedique a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="239e3-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="239e3-117">Si se generan devoluciones de llamada de posición más rápidamente de lo que la aplicación puede procesar, el miembro **dwOffset** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) podría hacer referencia a un evento que la aplicación aún no ha procesado.</span><span class="sxs-lookup"><span data-stu-id="239e3-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="239e3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="239e3-118">Requirements</span></span>



| <span data-ttu-id="239e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="239e3-119">Requirement</span></span> | <span data-ttu-id="239e3-120">Value</span><span class="sxs-lookup"><span data-stu-id="239e3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239e3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="239e3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="239e3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="239e3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="239e3-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="239e3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="239e3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="239e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="239e3-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="239e3-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239e3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="239e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239e3-128">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="239e3-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

