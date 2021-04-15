---
title: Mensaje de ICM_DRAW_FLUSH (VFW. h)
description: El \_ \_ mensaje de vaciado de dibujo de ICM notifica a un controlador de representación que represente el contenido de los búferes de imagen que están a la espera de ser dibujados. Puede enviar este mensaje explícitamente o mediante la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- Mensaje de ICM_DRAW_FLUSH de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676799"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="cc639-105">\_Mensaje de vaciado de dibujo de ICM \_</span><span class="sxs-lookup"><span data-stu-id="cc639-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="cc639-106">El mensaje de **\_ \_ vaciado de dibujo de ICM** notifica a un controlador de representación que represente el contenido de los búferes de imagen que están a la espera de ser dibujados.</span><span class="sxs-lookup"><span data-stu-id="cc639-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="cc639-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .</span><span class="sxs-lookup"><span data-stu-id="cc639-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cc639-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc639-108">Return Value</span></span>

<span data-ttu-id="cc639-109">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cc639-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc639-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc639-110">Remarks</span></span>

<span data-ttu-id="cc639-111">Este mensaje solo lo usa el hardware que realiza su propia descompresión asincrónica, temporización y dibujo.</span><span class="sxs-lookup"><span data-stu-id="cc639-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc639-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc639-112">Requirements</span></span>



| <span data-ttu-id="cc639-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc639-113">Requirement</span></span> | <span data-ttu-id="cc639-114">Value</span><span class="sxs-lookup"><span data-stu-id="cc639-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc639-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc639-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cc639-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cc639-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc639-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc639-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cc639-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc639-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc639-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc639-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc639-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc639-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc639-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc639-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc639-122">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="cc639-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="cc639-123">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="cc639-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





