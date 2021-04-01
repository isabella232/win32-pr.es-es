---
title: Mensaje de ICM_DRAW_RENDERBUFFER (VFW. h)
description: El mensaje RENDERBUFFER de ICM de \_ Draw \_ notifica a un controlador de representación que dibuje los fotogramas que se le han pasado. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Mensaje de ICM_DRAW_RENDERBUFFER de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996859"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="313e1-105">\_Mensaje RENDERBUFFER de Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="313e1-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="313e1-106">El **mensaje \_ \_ RENDERBUFFER de ICM de Draw** notifica a un controlador de representación que dibuje los fotogramas que se le han pasado.</span><span class="sxs-lookup"><span data-stu-id="313e1-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="313e1-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .</span><span class="sxs-lookup"><span data-stu-id="313e1-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="313e1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="313e1-108">Return Value</span></span>

<span data-ttu-id="313e1-109">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="313e1-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="313e1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="313e1-110">Remarks</span></span>

<span data-ttu-id="313e1-111">Use este mensaje con hardware que realice su propia descompresión asincrónica, temporización y dibujo.</span><span class="sxs-lookup"><span data-stu-id="313e1-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="313e1-112">Este mensaje se usa normalmente para realizar una operación de búsqueda cuando el controlador se debe indicar específicamente para mostrar cada fotograma de vídeo que se le ha pasado en lugar de reproducir una secuencia de fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="313e1-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="313e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313e1-113">Requirements</span></span>



| <span data-ttu-id="313e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="313e1-114">Requirement</span></span> | <span data-ttu-id="313e1-115">Value</span><span class="sxs-lookup"><span data-stu-id="313e1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="313e1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="313e1-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="313e1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="313e1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="313e1-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="313e1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="313e1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="313e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="313e1-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="313e1-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313e1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="313e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313e1-123">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="313e1-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="313e1-124">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="313e1-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





