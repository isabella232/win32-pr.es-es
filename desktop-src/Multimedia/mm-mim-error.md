---
title: Mensaje de MM_MIM_ERROR (mmsystem. h)
description: El \_ mensaje de error mm MIM \_ se envía a una ventana cuando se recibe un mensaje MIDI no válido.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- Mensaje de MM_MIM_ERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149970"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="8b532-104">Mensaje de error MM de \_ MIM \_</span><span class="sxs-lookup"><span data-stu-id="8b532-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="8b532-105">El mensaje de **\_ \_ error mm MIM** se envía a una ventana cuando se recibe un mensaje MIDI no válido.</span><span class="sxs-lookup"><span data-stu-id="8b532-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="8b532-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b532-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="8b532-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="8b532-108">Identificador del dispositivo de entrada MIDI que recibió el mensaje no válido.</span><span class="sxs-lookup"><span data-stu-id="8b532-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="8b532-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="8b532-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="8b532-110">Mensaje MIDI no válido.</span><span class="sxs-lookup"><span data-stu-id="8b532-110">Invalid MIDI message.</span></span> <span data-ttu-id="8b532-111">El mensaje se empaqueta en un valor **DWORD** con el primer byte del mensaje en el byte de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="8b532-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b532-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b532-112">Return Value</span></span>

<span data-ttu-id="8b532-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8b532-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b532-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b532-114">Requirements</span></span>



| <span data-ttu-id="8b532-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b532-115">Requirement</span></span> | <span data-ttu-id="8b532-116">Value</span><span class="sxs-lookup"><span data-stu-id="8b532-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b532-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b532-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b532-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b532-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b532-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b532-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b532-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b532-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b532-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b532-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b532-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b532-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b532-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b532-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b532-124">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="8b532-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8b532-125">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="8b532-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





