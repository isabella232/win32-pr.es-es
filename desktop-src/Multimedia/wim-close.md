---
title: Mensaje de WIM_CLOSE (mmsystem. h)
description: El \_ mensaje de cierre Wim se envía a la función de devolución de llamada de audio de forma de onda especificada cuando se cierra un dispositivo de entrada de audio de forma de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- Mensaje de WIM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492610"
---
# <a name="wim_close-message"></a><span data-ttu-id="299af-105">\_Mensaje de cierre Wim</span><span class="sxs-lookup"><span data-stu-id="299af-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="299af-106">El mensaje de **\_ cierre Wim** se envía a la función de devolución de llamada de audio de forma de onda especificada cuando se cierra un dispositivo de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="299af-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="299af-107">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="299af-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="299af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="299af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299af-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="299af-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="299af-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="299af-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="299af-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="299af-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="299af-112">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="299af-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299af-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="299af-113">Return Value</span></span>

<span data-ttu-id="299af-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="299af-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="299af-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="299af-115">Requirements</span></span>



| <span data-ttu-id="299af-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="299af-116">Requirement</span></span> | <span data-ttu-id="299af-117">Value</span><span class="sxs-lookup"><span data-stu-id="299af-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="299af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="299af-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="299af-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="299af-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="299af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="299af-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="299af-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="299af-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="299af-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="299af-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="299af-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299af-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="299af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299af-125">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="299af-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="299af-126">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="299af-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





