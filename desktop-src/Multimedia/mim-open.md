---
title: Mensaje de MIM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MIM se envía a una función de devolución de llamada de entrada MIDI cuando se abre un dispositivo de entrada MIDI.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- Mensaje de MIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421973"
---
# <a name="mim_open-message"></a><span data-ttu-id="a0306-104">\_Mensaje abierto de MIM</span><span class="sxs-lookup"><span data-stu-id="a0306-104">MIM\_OPEN message</span></span>

<span data-ttu-id="a0306-105">El **mensaje \_ abierto de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando se abre un dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0306-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="a0306-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0306-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a0306-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a0306-108">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="a0306-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="a0306-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a0306-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a0306-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="a0306-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0306-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0306-111">Return Value</span></span>

<span data-ttu-id="a0306-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a0306-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0306-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0306-113">Requirements</span></span>



| <span data-ttu-id="a0306-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0306-114">Requirement</span></span> | <span data-ttu-id="a0306-115">Value</span><span class="sxs-lookup"><span data-stu-id="a0306-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0306-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0306-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0306-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a0306-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a0306-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0306-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0306-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0306-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a0306-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0306-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0306-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0306-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0306-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0306-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0306-123">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="a0306-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a0306-124">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="a0306-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





