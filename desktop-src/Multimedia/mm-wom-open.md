---
title: Mensaje de MM_WOM_OPEN (mmsystem. h)
description: El \_ \_ mensaje abierto mm WOM se envía a una ventana cuando se abre el dispositivo de salida de audio de forma de onda determinado.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- Mensaje de MM_WOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151232"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="0ff80-104">\_ \_ Mensaje abierto mm WOM</span><span class="sxs-lookup"><span data-stu-id="0ff80-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="0ff80-105">El **mensaje \_ \_ abierto mm WOM** se envía a una ventana cuando se abre el dispositivo de salida de audio de forma de onda determinado.</span><span class="sxs-lookup"><span data-stu-id="0ff80-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0ff80-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ff80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff80-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="0ff80-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="0ff80-108">Identificador del dispositivo que se abrió.</span><span class="sxs-lookup"><span data-stu-id="0ff80-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="0ff80-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ff80-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0ff80-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0ff80-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff80-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ff80-111">Return Value</span></span>

<span data-ttu-id="0ff80-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0ff80-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff80-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ff80-113">Requirements</span></span>



| <span data-ttu-id="0ff80-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ff80-114">Requirement</span></span> | <span data-ttu-id="0ff80-115">Value</span><span class="sxs-lookup"><span data-stu-id="0ff80-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff80-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ff80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff80-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0ff80-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0ff80-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ff80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff80-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ff80-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0ff80-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ff80-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ff80-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff80-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff80-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ff80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff80-123">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="0ff80-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="0ff80-124">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="0ff80-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





