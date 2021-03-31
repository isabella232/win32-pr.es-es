---
title: Mensaje de WOM_OPEN (mmsystem. h)
description: El \_ mensaje abierto WOM se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se abre un dispositivo de salida de audio de forma de onda.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- Mensaje de WOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149871"
---
# <a name="wom_open-message"></a><span data-ttu-id="14d0e-104">WOM \_ abrir mensaje</span><span class="sxs-lookup"><span data-stu-id="14d0e-104">WOM\_OPEN message</span></span>

<span data-ttu-id="14d0e-105">El **mensaje \_ abierto WOM** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se abre un dispositivo de salida de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="14d0e-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="14d0e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d0e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="14d0e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="14d0e-108">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="14d0e-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="14d0e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="14d0e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="14d0e-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="14d0e-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d0e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14d0e-111">Return Value</span></span>

<span data-ttu-id="14d0e-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="14d0e-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d0e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d0e-113">Requirements</span></span>



| <span data-ttu-id="14d0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d0e-114">Requirement</span></span> | <span data-ttu-id="14d0e-115">Value</span><span class="sxs-lookup"><span data-stu-id="14d0e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d0e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="14d0e-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14d0e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14d0e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="14d0e-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14d0e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14d0e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14d0e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d0e-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14d0e-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d0e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="14d0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d0e-123">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="14d0e-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="14d0e-124">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="14d0e-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





