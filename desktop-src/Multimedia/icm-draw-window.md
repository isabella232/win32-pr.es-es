---
title: Mensaje de ICM_DRAW_WINDOW (VFW. h)
description: El mensaje de la \_ \_ ventana de dibujo ICM notifica a un controlador de representación que la ventana especificada para el mensaje de inicio de Draw de ICM \_ \_ debe volver a dibujarse.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- Mensaje de ICM_DRAW_WINDOW de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490133"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="daaef-104">Mensaje de ventana de \_ dibujo ICM \_</span><span class="sxs-lookup"><span data-stu-id="daaef-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="daaef-105">El mensaje de la **\_ \_ ventana de dibujo ICM** notifica a un controlador de representación que la ventana especificada para el mensaje de [**Inicio de \_ Draw \_ de ICM**](icm-draw-begin.md) debe volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="daaef-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="daaef-106">La ventana se ha cambiado o se ha ocultado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="daaef-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="daaef-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .</span><span class="sxs-lookup"><span data-stu-id="daaef-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="daaef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daaef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daaef-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="daaef-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="daaef-110">Puntero al rectángulo de destino en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="daaef-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="daaef-111">Si este parámetro señala a un rectángulo vacío, el dibujo debe estar desactivado.</span><span class="sxs-lookup"><span data-stu-id="daaef-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daaef-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daaef-112">Return Value</span></span>

<span data-ttu-id="daaef-113">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="daaef-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="daaef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daaef-114">Remarks</span></span>

<span data-ttu-id="daaef-115">Este mensaje es compatible con hardware que realiza su propia descompresión, temporización y dibujo asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="daaef-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="daaef-116">Los controladores de superposición de vídeo usan este mensaje para dibujar cuando la ventana se oculta o se mueve.</span><span class="sxs-lookup"><span data-stu-id="daaef-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="daaef-117">Cuando una ventana especificada para [**el \_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) está totalmente oculta en otras ventanas, el rectángulo de destino está vacío.</span><span class="sxs-lookup"><span data-stu-id="daaef-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="daaef-118">Los controladores deben desactivar el hardware de superposición de vídeo cuando se produce esta condición.</span><span class="sxs-lookup"><span data-stu-id="daaef-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="daaef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daaef-119">Requirements</span></span>



| <span data-ttu-id="daaef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="daaef-120">Requirement</span></span> | <span data-ttu-id="daaef-121">Value</span><span class="sxs-lookup"><span data-stu-id="daaef-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="daaef-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daaef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="daaef-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="daaef-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="daaef-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daaef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="daaef-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="daaef-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="daaef-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daaef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="daaef-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="daaef-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daaef-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="daaef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daaef-129">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="daaef-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="daaef-130">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="daaef-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





