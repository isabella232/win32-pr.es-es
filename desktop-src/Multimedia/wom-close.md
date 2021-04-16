---
title: Mensaje de WOM_CLOSE (mmsystem. h)
description: El \_ mensaje de cierre WOM se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se cierra un dispositivo de salida de audio de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- Mensaje de WOM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676699"
---
# <a name="wom_close-message"></a><span data-ttu-id="39a60-105">WOM \_ cerrar mensaje</span><span class="sxs-lookup"><span data-stu-id="39a60-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="39a60-106">El mensaje de **\_ cierre WOM** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se cierra un dispositivo de salida de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="39a60-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="39a60-107">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="39a60-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="39a60-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39a60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a60-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="39a60-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="39a60-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="39a60-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="39a60-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="39a60-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="39a60-112">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="39a60-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a60-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39a60-113">Return Value</span></span>

<span data-ttu-id="39a60-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="39a60-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a60-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a60-115">Requirements</span></span>



| <span data-ttu-id="39a60-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a60-116">Requirement</span></span> | <span data-ttu-id="39a60-117">Value</span><span class="sxs-lookup"><span data-stu-id="39a60-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a60-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39a60-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39a60-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="39a60-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39a60-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39a60-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="39a60-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39a60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a60-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39a60-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a60-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="39a60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a60-125">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="39a60-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="39a60-126">Mensajes de onda</span><span class="sxs-lookup"><span data-stu-id="39a60-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





