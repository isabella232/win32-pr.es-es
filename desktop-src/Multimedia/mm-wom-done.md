---
title: Mensaje de MM_WOM_DONE (mmsystem. h)
description: El \_ mensaje mm WOM \_ done se envía a una ventana cuando el búfer de salida especificado se devuelve a la aplicación. Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la función waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- Mensaje de MM_WOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804087"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="10cf6-105">Mensaje de MM \_ WOM \_ Done</span><span class="sxs-lookup"><span data-stu-id="10cf6-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="10cf6-106">El mensaje **mm \_ WOM \_ Done** se envía a una ventana cuando el búfer de salida especificado se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10cf6-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="10cf6-107">Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="10cf6-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="10cf6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10cf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10cf6-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="10cf6-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="10cf6-110">Identificador del dispositivo de salida de onda y audio que reprodujo el búfer.</span><span class="sxs-lookup"><span data-stu-id="10cf6-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="10cf6-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="10cf6-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="10cf6-112">Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="10cf6-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10cf6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10cf6-113">Return Value</span></span>

<span data-ttu-id="10cf6-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="10cf6-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10cf6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10cf6-115">Requirements</span></span>



| <span data-ttu-id="10cf6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10cf6-116">Requirement</span></span> | <span data-ttu-id="10cf6-117">Value</span><span class="sxs-lookup"><span data-stu-id="10cf6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cf6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10cf6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10cf6-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="10cf6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10cf6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10cf6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10cf6-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10cf6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10cf6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10cf6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10cf6-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10cf6-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10cf6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="10cf6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cf6-125">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="10cf6-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="10cf6-126">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="10cf6-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

