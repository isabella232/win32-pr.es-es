---
title: Mensaje de ICM_DRAW_STOP_PLAY (VFW. h)
description: El \_ mensaje ICM Draw \_ Stop \_ Play notifica a un controlador de representación cuando se completa una operación de reproducción. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Mensaje de ICM_DRAW_STOP_PLAY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151243"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="e6692-105">\_ \_ Mostrar mensaje de detención de \_ reproducción de ICM</span><span class="sxs-lookup"><span data-stu-id="e6692-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="e6692-106">El mensaje **ICM \_ Draw \_ Stop \_ Play** notifica a un controlador de representación cuando se completa una operación de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e6692-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="e6692-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .</span><span class="sxs-lookup"><span data-stu-id="e6692-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6692-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6692-108">Return Value</span></span>

<span data-ttu-id="e6692-109">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6692-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6692-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6692-110">Remarks</span></span>

<span data-ttu-id="e6692-111">Use este mensaje cuando se complete la operación de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e6692-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="e6692-112">Use el [**mensaje \_ \_ detener dibujo de ICM**](icm-draw-stop.md) para finalizar la temporización.</span><span class="sxs-lookup"><span data-stu-id="e6692-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6692-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6692-113">Requirements</span></span>



| <span data-ttu-id="e6692-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6692-114">Requirement</span></span> | <span data-ttu-id="e6692-115">Value</span><span class="sxs-lookup"><span data-stu-id="e6692-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6692-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6692-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6692-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e6692-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6692-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6692-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6692-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6692-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6692-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6692-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6692-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6692-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6692-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6692-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6692-123">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e6692-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e6692-124">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e6692-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





