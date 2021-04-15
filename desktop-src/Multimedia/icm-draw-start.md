---
title: Mensaje de ICM_DRAW_START (VFW. h)
description: El mensaje de inicio de Draw de ICM \_ \_ notifica a un controlador de representación que inicie su reloj interno durante el tiempo de dibujo de los marcos. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Mensaje de ICM_DRAW_START de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422225"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="e5c22-105">Mensaje de inicio de \_ Draw de ICM \_</span><span class="sxs-lookup"><span data-stu-id="e5c22-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="e5c22-106">El mensaje de **\_ \_ Inicio de Draw de ICM** notifica a un controlador de representación que inicie su reloj interno durante el tiempo de dibujo de los marcos.</span><span class="sxs-lookup"><span data-stu-id="e5c22-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="e5c22-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .</span><span class="sxs-lookup"><span data-stu-id="e5c22-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e5c22-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5c22-108">Return Value</span></span>

<span data-ttu-id="e5c22-109">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e5c22-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c22-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5c22-110">Remarks</span></span>

<span data-ttu-id="e5c22-111">Este mensaje lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.</span><span class="sxs-lookup"><span data-stu-id="e5c22-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="e5c22-112">Cuando el controlador recibe este mensaje, debe empezar a representar los datos a la velocidad especificada con el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c22-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="e5c22-113">Los mensajes de [**\_ \_ detención**](icm-draw-stop.md) de **\_ \_ Inicio** y de dibujo de ICM de ICM no se anidan.</span><span class="sxs-lookup"><span data-stu-id="e5c22-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="e5c22-114">Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la representación con la **\_ \_ detención de Draw ICM**, debe reiniciar la representación con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="e5c22-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5c22-115">Requirements</span></span>



| <span data-ttu-id="e5c22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c22-116">Requirement</span></span> | <span data-ttu-id="e5c22-117">Value</span><span class="sxs-lookup"><span data-stu-id="e5c22-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5c22-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5c22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c22-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5c22-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e5c22-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5c22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c22-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5c22-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5c22-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5c22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c22-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c22-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c22-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5c22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c22-125">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5c22-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e5c22-126">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5c22-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





