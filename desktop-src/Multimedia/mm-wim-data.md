---
title: Mensaje de MM_WIM_DATA (mmsystem. h)
description: El \_ mensaje de datos Wim de mm \_ se envía a una ventana cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación. El mensaje se puede enviar cuando el búfer esté lleno o después de que se llame a la función waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- Mensaje de MM_WIM_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686197"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="eefeb-105">\_Mensaje de \_ datos Wim mm</span><span class="sxs-lookup"><span data-stu-id="eefeb-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="eefeb-106">El mensaje de **\_ \_ datos Wim de mm** se envía a una ventana cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eefeb-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="eefeb-107">El mensaje se puede enviar cuando el búfer esté lleno o después de que se llame a la función [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="eefeb-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="eefeb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eefeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefeb-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="eefeb-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="eefeb-110">Identificador del dispositivo de entrada de onda-audio que recibió los datos.</span><span class="sxs-lookup"><span data-stu-id="eefeb-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="eefeb-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="eefeb-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="eefeb-112">Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="eefeb-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefeb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eefeb-113">Return Value</span></span>

<span data-ttu-id="eefeb-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eefeb-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefeb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eefeb-115">Remarks</span></span>

<span data-ttu-id="eefeb-116">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="eefeb-116">The returned buffer might not be full.</span></span> <span data-ttu-id="eefeb-117">Use el miembro **dwBytesRecorded** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lParam* para determinar el número de bytes grabados en el búfer devuelto.</span><span class="sxs-lookup"><span data-stu-id="eefeb-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="eefeb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eefeb-118">Requirements</span></span>



| <span data-ttu-id="eefeb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eefeb-119">Requirement</span></span> | <span data-ttu-id="eefeb-120">Value</span><span class="sxs-lookup"><span data-stu-id="eefeb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefeb-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eefeb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eefeb-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eefeb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eefeb-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eefeb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eefeb-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eefeb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eefeb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eefeb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eefeb-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eefeb-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefeb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eefeb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefeb-128">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="eefeb-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="eefeb-129">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="eefeb-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

