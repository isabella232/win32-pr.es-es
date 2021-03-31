---
title: Mensaje de MM_MIM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MIM de mm \_ se envía a una ventana cuando se abre un dispositivo de entrada MIDI.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- Mensaje de MM_MIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904978"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="4ece4-104">\_Mensaje abierto de MIM de mm \_</span><span class="sxs-lookup"><span data-stu-id="4ece4-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="4ece4-105">El **mensaje \_ \_ abierto de MIM de mm** se envía a una ventana cuando se abre un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ece4-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="4ece4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ece4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ece4-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="4ece4-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4ece4-108">Identificador del dispositivo de entrada MIDI que se abrió.</span><span class="sxs-lookup"><span data-stu-id="4ece4-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="4ece4-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ece4-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4ece4-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="4ece4-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ece4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ece4-111">Return Value</span></span>

<span data-ttu-id="4ece4-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ece4-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ece4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ece4-113">Requirements</span></span>



| <span data-ttu-id="4ece4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ece4-114">Requirement</span></span> | <span data-ttu-id="4ece4-115">Value</span><span class="sxs-lookup"><span data-stu-id="4ece4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ece4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ece4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ece4-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ece4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ece4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ece4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ece4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ece4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ece4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ece4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ece4-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ece4-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ece4-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ece4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ece4-123">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4ece4-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4ece4-124">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="4ece4-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





