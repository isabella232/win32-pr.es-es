---
title: Mensaje de MM_WIM_OPEN (mmsystem. h)
description: El \_ mensaje de apertura Wim de mm \_ se envía a una ventana cuando se abre un dispositivo de entrada de audio de forma de onda.
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- Mensaje de MM_WIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079771"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="28467-104">\_ \_ Mensaje abierto mm Wim</span><span class="sxs-lookup"><span data-stu-id="28467-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="28467-105">El mensaje de **\_ \_ apertura Wim de mm** se envía a una ventana cuando se abre un dispositivo de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="28467-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="28467-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28467-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="28467-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="28467-108">Identificador del dispositivo que se abrió.</span><span class="sxs-lookup"><span data-stu-id="28467-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="28467-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="28467-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="28467-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="28467-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28467-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28467-111">Return Value</span></span>

<span data-ttu-id="28467-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28467-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28467-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28467-113">Requirements</span></span>



| <span data-ttu-id="28467-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28467-114">Requirement</span></span> | <span data-ttu-id="28467-115">Value</span><span class="sxs-lookup"><span data-stu-id="28467-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28467-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28467-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28467-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28467-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28467-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28467-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28467-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28467-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28467-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28467-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28467-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28467-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28467-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="28467-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28467-123">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="28467-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="28467-124">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="28467-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





