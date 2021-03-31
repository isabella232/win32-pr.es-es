---
title: Mensaje de ICM_DRAW_START_PLAY (VFW. h)
description: El \_ \_ \_ mensaje de reproducción para el inicio de Draw ICM proporciona las horas de inicio y finalización de una operación de reproducción a un controlador de representación. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Mensaje de ICM_DRAW_START_PLAY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150178"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="f1b05-105">Reinicio de la \_ reproducción del dibujo ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1b05-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="f1b05-106">El mensaje de reproducción para el **\_ Inicio de Draw \_ \_ ICM** proporciona las horas de inicio y finalización de una operación de reproducción a un controlador de representación.</span><span class="sxs-lookup"><span data-stu-id="f1b05-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="f1b05-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .</span><span class="sxs-lookup"><span data-stu-id="f1b05-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="f1b05-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1b05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b05-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span><span class="sxs-lookup"><span data-stu-id="f1b05-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="f1b05-110">Hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="f1b05-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="f1b05-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*Cartuchos*</span><span class="sxs-lookup"><span data-stu-id="f1b05-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="f1b05-112">Hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="f1b05-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b05-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b05-113">Return Value</span></span>

<span data-ttu-id="f1b05-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f1b05-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b05-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1b05-115">Remarks</span></span>

<span data-ttu-id="f1b05-116">Este mensaje precede a los datos de fotogramas enviados al controlador de representación.</span><span class="sxs-lookup"><span data-stu-id="f1b05-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="f1b05-117">Las unidades de *lFrom* y *lTo* se especifican con el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="f1b05-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="f1b05-118">En el caso de los datos de vídeo, suele ser un número de marco.</span><span class="sxs-lookup"><span data-stu-id="f1b05-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="f1b05-119">Para obtener más información sobre la velocidad de reproducción, vea los miembros **dwRate** y **dwScale** de la estructura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .</span><span class="sxs-lookup"><span data-stu-id="f1b05-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="f1b05-120">Si la hora de finalización es menor que la hora de inicio, se invierte la dirección de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f1b05-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b05-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b05-121">Requirements</span></span>



| <span data-ttu-id="f1b05-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b05-122">Requirement</span></span> | <span data-ttu-id="f1b05-123">Value</span><span class="sxs-lookup"><span data-stu-id="f1b05-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1b05-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1b05-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b05-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f1b05-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1b05-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1b05-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b05-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1b05-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1b05-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1b05-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b05-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b05-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b05-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1b05-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b05-131">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f1b05-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f1b05-132">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f1b05-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





