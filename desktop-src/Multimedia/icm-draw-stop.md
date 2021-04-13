---
title: Mensaje de ICM_DRAW_STOP (VFW. h)
description: El \_ \_ mensaje detener dibujo de ICM notifica a un controlador de representación que detenga su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- Mensaje de ICM_DRAW_STOP de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490138"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="dd2db-105">Mensaje de detención de \_ Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="dd2db-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="dd2db-106">El **mensaje \_ \_ detener dibujo de ICM** notifica a un controlador de representación que detenga su reloj interno durante el tiempo de dibujo de los marcos.</span><span class="sxs-lookup"><span data-stu-id="dd2db-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="dd2db-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .</span><span class="sxs-lookup"><span data-stu-id="dd2db-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="dd2db-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd2db-108">Return Value</span></span>

<span data-ttu-id="dd2db-109">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dd2db-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2db-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd2db-110">Remarks</span></span>

<span data-ttu-id="dd2db-111">Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.</span><span class="sxs-lookup"><span data-stu-id="dd2db-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2db-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd2db-112">Requirements</span></span>



| <span data-ttu-id="dd2db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd2db-113">Requirement</span></span> | <span data-ttu-id="dd2db-114">Value</span><span class="sxs-lookup"><span data-stu-id="dd2db-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dd2db-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2db-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd2db-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dd2db-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2db-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2db-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd2db-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd2db-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd2db-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2db-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2db-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2db-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd2db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2db-122">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="dd2db-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="dd2db-123">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="dd2db-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





