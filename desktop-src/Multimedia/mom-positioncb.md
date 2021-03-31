---
title: Mensaje de MOM_POSITIONCB (mmsystem. h)
description: El mensaje de posición de MOM \_ se envía cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- Mensaje de MOM_POSITIONCB de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803667"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="28230-104">Mensaje de POSITIONCB de MOM \_</span><span class="sxs-lookup"><span data-stu-id="28230-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="28230-105">El mensaje de **\_ posición de MOM** se envía cuando se alcanza un evento de **devolución de \_ \_ llamada de MEVT F** en el flujo de salida de MIDI.</span><span class="sxs-lookup"><span data-stu-id="28230-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="28230-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28230-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="28230-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="28230-108">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="28230-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="28230-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="28230-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="28230-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="28230-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28230-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28230-111">Return Value</span></span>

<span data-ttu-id="28230-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28230-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28230-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28230-113">Remarks</span></span>

<span data-ttu-id="28230-114">La reproducción del búfer de secuencia continúa incluso mientras se ejecuta la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="28230-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="28230-115">Todos los eventos después del evento de **\_ devolución de \_ llamada de MEVT F** en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedique a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="28230-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="28230-116">Si se generan devoluciones de llamada de posición más rápidamente de lo que la aplicación puede procesar, el miembro **dwOffset** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) podría hacer referencia a un evento que la aplicación aún no ha procesado.</span><span class="sxs-lookup"><span data-stu-id="28230-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="28230-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28230-117">Requirements</span></span>



| <span data-ttu-id="28230-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="28230-118">Requirement</span></span> | <span data-ttu-id="28230-119">Value</span><span class="sxs-lookup"><span data-stu-id="28230-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28230-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28230-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28230-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28230-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28230-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28230-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28230-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28230-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28230-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28230-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28230-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28230-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28230-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="28230-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28230-127">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="28230-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

