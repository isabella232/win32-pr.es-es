---
title: Mensaje de ICM_DRAW_SETTIME (VFW. h)
description: El \_ \_ control SETTIME de ICM proporciona información de sincronización a un controlador de representación que controla el tiempo de dibujo de los marcos.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Mensaje de ICM_DRAW_SETTIME de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905160"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="772e1-104">Desdibujado ICM \_ \_ mensaje SETTIME</span><span class="sxs-lookup"><span data-stu-id="772e1-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="772e1-105">El **control \_ \_ SETTIME de ICM** proporciona información de sincronización a un controlador de representación que controla el tiempo de dibujo de los marcos.</span><span class="sxs-lookup"><span data-stu-id="772e1-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="772e1-106">La información de sincronización es el número de muestra del marco que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="772e1-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="772e1-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .</span><span class="sxs-lookup"><span data-stu-id="772e1-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="772e1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="772e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772e1-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span><span class="sxs-lookup"><span data-stu-id="772e1-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="772e1-110">Número de muestra del marco que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="772e1-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772e1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="772e1-111">Return Value</span></span>

<span data-ttu-id="772e1-112">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="772e1-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="772e1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="772e1-113">Remarks</span></span>

<span data-ttu-id="772e1-114">Normalmente, el controlador compara el valor especificado con el número de marco asociado a la hora de su reloj interno e intenta sincronizar los dos si la diferencia es significativa.</span><span class="sxs-lookup"><span data-stu-id="772e1-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="772e1-115">Utilice este mensaje cuando el hardware realice su propia descompresión asincrónica, temporización y dibujo, y el hardware se base en una señal de sincronización externa (el hardware no se utiliza como maestro de sincronización).</span><span class="sxs-lookup"><span data-stu-id="772e1-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="772e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="772e1-116">Requirements</span></span>



| <span data-ttu-id="772e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="772e1-117">Requirement</span></span> | <span data-ttu-id="772e1-118">Value</span><span class="sxs-lookup"><span data-stu-id="772e1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="772e1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="772e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="772e1-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="772e1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="772e1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="772e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="772e1-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="772e1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="772e1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="772e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="772e1-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="772e1-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="772e1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="772e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772e1-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="772e1-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="772e1-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="772e1-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





