---
title: Mensaje de WM_CAP_SET_PREVIEWRATE (VFW. h)
description: El \_ \_ mensaje PREVIEWRATE del conjunto de límites de WM \_ establece la velocidad de presentación del marco en el modo de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Mensaje de WM_CAP_SET_PREVIEWRATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997058"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="7a976-105">\_ \_ Mensaje PREVIEWRATE de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="7a976-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="7a976-106">El **mensaje \_ \_ \_ PREVIEWRATE del conjunto de límites de WM** establece la velocidad de presentación del marco en el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="7a976-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="7a976-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .</span><span class="sxs-lookup"><span data-stu-id="7a976-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="7a976-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a976-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a976-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="7a976-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="7a976-110">Velocidad, en milisegundos, a la que se capturan y muestran los nuevos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="7a976-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a976-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a976-111">Return Value</span></span>

<span data-ttu-id="7a976-112">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="7a976-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a976-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a976-113">Remarks</span></span>

<span data-ttu-id="7a976-114">El modo de vista previa utiliza recursos de CPU importantes.</span><span class="sxs-lookup"><span data-stu-id="7a976-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="7a976-115">Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="7a976-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="7a976-116">Durante la captura de vídeo en streaming, la tarea de vista previa tiene una prioridad más baja que la escritura de tramas en el disco, y los marcos de vista previa solo se muestran si no hay otros búferes disponibles para escritura.</span><span class="sxs-lookup"><span data-stu-id="7a976-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a976-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a976-117">Requirements</span></span>



| <span data-ttu-id="7a976-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a976-118">Requirement</span></span> | <span data-ttu-id="7a976-119">Value</span><span class="sxs-lookup"><span data-stu-id="7a976-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a976-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a976-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a976-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a976-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7a976-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a976-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a976-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a976-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7a976-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a976-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a976-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a976-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a976-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a976-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a976-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7a976-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7a976-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7a976-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





