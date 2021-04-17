---
title: Mensaje de MIM_CLOSE (mmsystem. h)
description: El mensaje de cierre de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando se cierra un dispositivo de entrada MIDI.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- Mensaje de MIM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533795"
---
# <a name="mim_close-message"></a><span data-ttu-id="df47a-104">Mensaje de cierre de MIM \_</span><span class="sxs-lookup"><span data-stu-id="df47a-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="df47a-105">El mensaje de **\_ cierre de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando se cierra un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="df47a-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="df47a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df47a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df47a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="df47a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="df47a-108">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="df47a-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="df47a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="df47a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="df47a-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="df47a-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df47a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df47a-111">Return Value</span></span>

<span data-ttu-id="df47a-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="df47a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df47a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df47a-113">Remarks</span></span>

<span data-ttu-id="df47a-114">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="df47a-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="df47a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df47a-115">Requirements</span></span>



| <span data-ttu-id="df47a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df47a-116">Requirement</span></span> | <span data-ttu-id="df47a-117">Value</span><span class="sxs-lookup"><span data-stu-id="df47a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df47a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df47a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df47a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df47a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df47a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df47a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df47a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df47a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df47a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df47a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df47a-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df47a-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df47a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="df47a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df47a-125">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="df47a-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="df47a-126">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="df47a-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





