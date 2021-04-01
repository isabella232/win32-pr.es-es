---
title: Mensaje de MOM_CLOSE (mmsystem. h)
description: El mensaje de cierre de MOM \_ se envía a una función de devolución de llamada de salida MIDI cuando se cierra un dispositivo de salida MIDI.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- Mensaje de MOM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997010"
---
# <a name="mom_close-message"></a><span data-ttu-id="1a7d3-104">Mensaje de cierre de MOM \_</span><span class="sxs-lookup"><span data-stu-id="1a7d3-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="1a7d3-105">El mensaje de **\_ cierre de MOM** se envía a una función de devolución de llamada de salida MIDI cuando se cierra un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="1a7d3-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1a7d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a7d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7d3-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1a7d3-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a7d3-108">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="1a7d3-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="1a7d3-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1a7d3-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a7d3-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="1a7d3-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7d3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a7d3-111">Return Value</span></span>

<span data-ttu-id="1a7d3-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1a7d3-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a7d3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a7d3-113">Remarks</span></span>

<span data-ttu-id="1a7d3-114">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1a7d3-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a7d3-115">Requirements</span></span>



| <span data-ttu-id="1a7d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a7d3-116">Requirement</span></span> | <span data-ttu-id="1a7d3-117">Value</span><span class="sxs-lookup"><span data-stu-id="1a7d3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7d3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a7d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7d3-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1a7d3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a7d3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a7d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7d3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a7d3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1a7d3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a7d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a7d3-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a7d3-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a7d3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a7d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7d3-125">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="1a7d3-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





