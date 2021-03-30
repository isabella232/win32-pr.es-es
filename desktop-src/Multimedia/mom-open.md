---
title: Mensaje de MOM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MOM se envía a una función de devolución de llamada de salida MIDI cuando se abre un dispositivo de salida MIDI.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- Mensaje de MOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803673"
---
# <a name="mom_open-message"></a><span data-ttu-id="8c13a-104">\_Mensaje abierto de MOM</span><span class="sxs-lookup"><span data-stu-id="8c13a-104">MOM\_OPEN message</span></span>

<span data-ttu-id="8c13a-105">El **mensaje \_ abierto de MOM** se envía a una función de devolución de llamada de salida MIDI cuando se abre un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="8c13a-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8c13a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c13a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8c13a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8c13a-108">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="8c13a-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="8c13a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8c13a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8c13a-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="8c13a-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c13a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c13a-111">Return Value</span></span>

<span data-ttu-id="8c13a-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c13a-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c13a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c13a-113">Requirements</span></span>



| <span data-ttu-id="8c13a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c13a-114">Requirement</span></span> | <span data-ttu-id="8c13a-115">Value</span><span class="sxs-lookup"><span data-stu-id="8c13a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c13a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c13a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c13a-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c13a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c13a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c13a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c13a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c13a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c13a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c13a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c13a-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c13a-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c13a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c13a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c13a-123">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="8c13a-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





