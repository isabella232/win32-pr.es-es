---
title: Mensaje de MM_WOM_CLOSE (mmsystem. h)
description: El \_ mensaje de cierre mm WOM \_ se envía a una ventana cuando se cierra un dispositivo de salida de audio de forma de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- Mensaje de MM_WOM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686254"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="bb74c-105">Mensaje de cierre de MM \_ WOM \_</span><span class="sxs-lookup"><span data-stu-id="bb74c-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="bb74c-106">El mensaje de **\_ \_ cierre mm WOM** se envía a una ventana cuando se cierra un dispositivo de salida de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="bb74c-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="bb74c-107">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="bb74c-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="bb74c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb74c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb74c-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="bb74c-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="bb74c-110">Identificador del dispositivo que se cerró.</span><span class="sxs-lookup"><span data-stu-id="bb74c-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="bb74c-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb74c-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="bb74c-112">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bb74c-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb74c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb74c-113">Return Value</span></span>

<span data-ttu-id="bb74c-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bb74c-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb74c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb74c-115">Requirements</span></span>



| <span data-ttu-id="bb74c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb74c-116">Requirement</span></span> | <span data-ttu-id="bb74c-117">Value</span><span class="sxs-lookup"><span data-stu-id="bb74c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb74c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb74c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb74c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb74c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb74c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb74c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb74c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb74c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb74c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb74c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb74c-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb74c-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb74c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb74c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb74c-125">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="bb74c-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="bb74c-126">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="bb74c-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





