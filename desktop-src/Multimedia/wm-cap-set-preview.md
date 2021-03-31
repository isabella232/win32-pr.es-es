---
title: Mensaje de WM_CAP_SET_PREVIEW (VFW. h)
description: El \_ mensaje de vista previa del límite de Cap de WM \_ \_ habilita o deshabilita el modo de vista previa.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Mensaje de WM_CAP_SET_PREVIEW de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151097"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="1e9c9-104">\_Mensaje de \_ \_ vista previa de límite de Cap de WM</span><span class="sxs-lookup"><span data-stu-id="1e9c9-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="1e9c9-105">El mensaje de **\_ \_ \_ vista previa del límite de Cap de WM** habilita o deshabilita el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="1e9c9-106">En el modo de vista previa, los fotogramas se transfieren del hardware de captura a la memoria del sistema y, a continuación, se muestran en la ventana de captura mediante funciones GDI.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="1e9c9-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .</span><span class="sxs-lookup"><span data-stu-id="1e9c9-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="1e9c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e9c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9c9-109"><span id="f"></span><span id="F"></span>*formato*</span><span class="sxs-lookup"><span data-stu-id="1e9c9-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="1e9c9-110">Marca de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-110">Preview flag.</span></span> <span data-ttu-id="1e9c9-111">Especifique **true** para que este parámetro habilite el modo de vista previa o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9c9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e9c9-112">Return Value</span></span>

<span data-ttu-id="1e9c9-113">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e9c9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e9c9-114">Remarks</span></span>

<span data-ttu-id="1e9c9-115">El modo de vista previa utiliza recursos de CPU importantes.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="1e9c9-116">Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="1e9c9-117">El miembro **fLiveWindow** de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de vista previa está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="1e9c9-118">Al habilitar el modo de vista previa se deshabilita automáticamente el modo de superposición.</span><span class="sxs-lookup"><span data-stu-id="1e9c9-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9c9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e9c9-119">Requirements</span></span>



| <span data-ttu-id="1e9c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e9c9-120">Requirement</span></span> | <span data-ttu-id="1e9c9-121">Value</span><span class="sxs-lookup"><span data-stu-id="1e9c9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1e9c9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e9c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9c9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e9c9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1e9c9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e9c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9c9-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e9c9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1e9c9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e9c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e9c9-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e9c9-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9c9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e9c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9c9-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1e9c9-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1e9c9-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1e9c9-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





