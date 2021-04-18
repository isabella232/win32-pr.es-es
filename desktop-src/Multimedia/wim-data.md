---
title: Mensaje de WIM_DATA (mmsystem. h)
description: El \_ mensaje de datos Wim se envía a la función de devolución de llamada de entrada de audio de forma de onda especificada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- Mensaje de WIM_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676907"
---
# <a name="wim_data-message"></a><span data-ttu-id="1356c-104">\_Mensaje de datos Wim</span><span class="sxs-lookup"><span data-stu-id="1356c-104">WIM\_DATA message</span></span>

<span data-ttu-id="1356c-105">El mensaje de **\_ datos Wim** se envía a la función de devolución de llamada de entrada de audio de forma de onda especificada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1356c-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="1356c-106">Se puede enviar el mensaje cuando el búfer esté lleno o después de que se llame a la función [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="1356c-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1356c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1356c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1356c-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1356c-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1356c-109">Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="1356c-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="1356c-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1356c-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1356c-111">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1356c-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1356c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1356c-112">Return Value</span></span>

<span data-ttu-id="1356c-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1356c-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1356c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1356c-114">Remarks</span></span>

<span data-ttu-id="1356c-115">Es posible que el búfer devuelto no esté lleno.</span><span class="sxs-lookup"><span data-stu-id="1356c-115">The returned buffer might not be full.</span></span> <span data-ttu-id="1356c-116">Use el miembro **dwBytesRecorded** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lpwvhdr* para determinar el número de bytes grabados en el búfer devuelto.</span><span class="sxs-lookup"><span data-stu-id="1356c-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1356c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1356c-117">Requirements</span></span>



| <span data-ttu-id="1356c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1356c-118">Requirement</span></span> | <span data-ttu-id="1356c-119">Value</span><span class="sxs-lookup"><span data-stu-id="1356c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1356c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1356c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1356c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1356c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1356c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1356c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1356c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1356c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1356c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1356c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1356c-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1356c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1356c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1356c-127">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="1356c-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="1356c-128">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="1356c-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

