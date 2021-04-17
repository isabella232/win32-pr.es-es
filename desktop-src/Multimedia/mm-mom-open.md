---
title: Mensaje de MM_MOM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MOM de mm \_ se envía a una ventana cuando se abre un dispositivo de salida MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- Mensaje de MM_MOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488969"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="e2087-104">\_Mensaje abierto de MOM de mm \_</span><span class="sxs-lookup"><span data-stu-id="e2087-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="e2087-105">El **mensaje \_ \_ abierto de MOM de mm** se envía a una ventana cuando se abre un dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="e2087-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e2087-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2087-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2087-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="e2087-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="e2087-108">Identificador del dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="e2087-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="e2087-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2087-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e2087-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="e2087-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2087-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2087-111">Return Value</span></span>

<span data-ttu-id="e2087-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e2087-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2087-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2087-113">Requirements</span></span>



| <span data-ttu-id="e2087-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2087-114">Requirement</span></span> | <span data-ttu-id="e2087-115">Value</span><span class="sxs-lookup"><span data-stu-id="e2087-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2087-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2087-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2087-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e2087-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2087-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2087-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2087-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2087-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2087-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2087-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2087-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2087-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2087-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2087-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2087-123">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="e2087-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





