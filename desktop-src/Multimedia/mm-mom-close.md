---
title: Mensaje de MM_MOM_CLOSE (mmsystem. h)
description: El mensaje de cierre de MOM de MM \_ \_ se envía a una ventana cuando se cierra un dispositivo de salida MIDI.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- Mensaje de MM_MOM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489394"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="b08fe-104">Mensaje de cierre de MM \_ MOM \_</span><span class="sxs-lookup"><span data-stu-id="b08fe-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="b08fe-105">El mensaje de **\_ \_ cierre de MOM de mm** se envía a una ventana cuando se cierra un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="b08fe-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b08fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b08fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08fe-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="b08fe-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="b08fe-108">Identificador del dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="b08fe-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="b08fe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b08fe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b08fe-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="b08fe-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b08fe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b08fe-111">Return Value</span></span>

<span data-ttu-id="b08fe-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b08fe-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b08fe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b08fe-113">Remarks</span></span>

<span data-ttu-id="b08fe-114">El identificador de dispositivo ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b08fe-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08fe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b08fe-115">Requirements</span></span>



| <span data-ttu-id="b08fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b08fe-116">Requirement</span></span> | <span data-ttu-id="b08fe-117">Value</span><span class="sxs-lookup"><span data-stu-id="b08fe-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08fe-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b08fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b08fe-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b08fe-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b08fe-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b08fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b08fe-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b08fe-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b08fe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b08fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b08fe-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b08fe-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b08fe-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b08fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08fe-125">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="b08fe-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





