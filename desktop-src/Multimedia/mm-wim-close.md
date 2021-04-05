---
title: Mensaje de MM_WIM_CLOSE (mmsystem. h)
description: El \_ mensaje de cierre Wim de mm \_ se envía a una ventana cuando se cierra un dispositivo de entrada de audio de forma de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- Mensaje de MM_WIM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078836"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="3cba3-105">Mensaje de cierre de \_ Wim mm \_</span><span class="sxs-lookup"><span data-stu-id="3cba3-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="3cba3-106">El mensaje de **\_ \_ cierre Wim de mm** se envía a una ventana cuando se cierra un dispositivo de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="3cba3-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="3cba3-107">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3cba3-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="3cba3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cba3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cba3-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="3cba3-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="3cba3-110">Identificador del dispositivo de entrada de onda-audio que se cerró.</span><span class="sxs-lookup"><span data-stu-id="3cba3-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="3cba3-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cba3-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3cba3-112">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3cba3-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cba3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cba3-113">Return Value</span></span>

<span data-ttu-id="3cba3-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3cba3-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cba3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cba3-115">Requirements</span></span>



| <span data-ttu-id="3cba3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cba3-116">Requirement</span></span> | <span data-ttu-id="3cba3-117">Value</span><span class="sxs-lookup"><span data-stu-id="3cba3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cba3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cba3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3cba3-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3cba3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3cba3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cba3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3cba3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3cba3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3cba3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cba3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cba3-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cba3-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cba3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cba3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cba3-125">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="3cba3-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="3cba3-126">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="3cba3-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





