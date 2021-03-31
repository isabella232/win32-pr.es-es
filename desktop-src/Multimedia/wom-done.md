---
title: Mensaje de WOM_DONE (mmsystem. h)
description: El \_ mensaje WOM done se envía a una función de devolución de llamada de salida de audio de forma de onda cuando el búfer de salida especificado se devuelve a la aplicación.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- Mensaje de WOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149966"
---
# <a name="wom_done-message"></a><span data-ttu-id="1cff5-104">Mensaje de WOM \_ Done</span><span class="sxs-lookup"><span data-stu-id="1cff5-104">WOM\_DONE message</span></span>

<span data-ttu-id="1cff5-105">El mensaje **WOM \_ Done** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando el búfer de salida especificado se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cff5-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="1cff5-106">Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="1cff5-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1cff5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cff5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cff5-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1cff5-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-109">Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="1cff5-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1cff5-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-111">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1cff5-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cff5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cff5-112">Return Value</span></span>

<span data-ttu-id="1cff5-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1cff5-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cff5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cff5-114">Requirements</span></span>



| <span data-ttu-id="1cff5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cff5-115">Requirement</span></span> | <span data-ttu-id="1cff5-116">Value</span><span class="sxs-lookup"><span data-stu-id="1cff5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cff5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cff5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1cff5-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1cff5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cff5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cff5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1cff5-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cff5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1cff5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cff5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cff5-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cff5-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cff5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cff5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cff5-124">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="1cff5-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="1cff5-125">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="1cff5-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

