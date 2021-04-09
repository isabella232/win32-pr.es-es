---
title: Mensaje de WIM_OPEN (mmsystem. h)
description: El \_ mensaje abierto Wim se envía a una función de devolución de llamada de entrada de audio de forma de onda cuando se abre un dispositivo de entrada de audio de forma de onda.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- Mensaje de WIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996949"
---
# <a name="wim_open-message"></a><span data-ttu-id="61cc7-104">\_Mensaje abierto Wim</span><span class="sxs-lookup"><span data-stu-id="61cc7-104">WIM\_OPEN message</span></span>

<span data-ttu-id="61cc7-105">El **mensaje \_ abierto Wim** se envía a una función de devolución de llamada de entrada de audio de forma de onda cuando se abre un dispositivo de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="61cc7-105">The **WIM\_OPEN** message is sent to a waveform-audio input callback function when a waveform-audio input device is opened.</span></span>


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="61cc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cc7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="61cc7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="61cc7-108">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="61cc7-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="61cc7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="61cc7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="61cc7-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="61cc7-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cc7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61cc7-111">Return Value</span></span>

<span data-ttu-id="61cc7-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61cc7-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cc7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cc7-113">Requirements</span></span>



| <span data-ttu-id="61cc7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cc7-114">Requirement</span></span> | <span data-ttu-id="61cc7-115">Value</span><span class="sxs-lookup"><span data-stu-id="61cc7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cc7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61cc7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61cc7-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="61cc7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="61cc7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61cc7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61cc7-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61cc7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61cc7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61cc7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61cc7-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61cc7-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cc7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="61cc7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cc7-123">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="61cc7-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="61cc7-124">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="61cc7-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





