---
title: Mensaje de MM_MIM_CLOSE (mmsystem. h)
description: El mensaje de cierre de MIM de MM \_ \_ se envía a una ventana cuando se cierra un dispositivo de entrada MIDI.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- Mensaje de MM_MIM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996696"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="6fa95-104">Mensaje de cierre de MM \_ MIM \_</span><span class="sxs-lookup"><span data-stu-id="6fa95-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="6fa95-105">El mensaje de **\_ \_ cierre de MIM de mm** se envía a una ventana cuando se cierra un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="6fa95-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6fa95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fa95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa95-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6fa95-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6fa95-108">Identificador del dispositivo de entrada MIDI que se cerró.</span><span class="sxs-lookup"><span data-stu-id="6fa95-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="6fa95-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fa95-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6fa95-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="6fa95-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa95-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fa95-111">Return Value</span></span>

<span data-ttu-id="6fa95-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6fa95-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa95-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fa95-113">Remarks</span></span>

<span data-ttu-id="6fa95-114">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="6fa95-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa95-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa95-115">Requirements</span></span>



| <span data-ttu-id="6fa95-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa95-116">Requirement</span></span> | <span data-ttu-id="6fa95-117">Value</span><span class="sxs-lookup"><span data-stu-id="6fa95-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa95-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fa95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa95-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6fa95-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6fa95-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fa95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa95-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fa95-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6fa95-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fa95-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa95-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fa95-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa95-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fa95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa95-125">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="6fa95-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6fa95-126">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="6fa95-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





