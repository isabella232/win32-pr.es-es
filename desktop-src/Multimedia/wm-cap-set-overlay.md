---
title: Mensaje de WM_CAP_SET_OVERLAY (VFW. h)
description: El \_ mensaje de superposición de conjunto de Cap de WM \_ \_ habilita o deshabilita el modo de superposición. En el modo de superposición, el vídeo se muestra mediante la superposición de hardware. Puede enviar este mensaje explícitamente o mediante la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- Mensaje de WM_CAP_SET_OVERLAY de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676963"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="ab767-106">\_Mensaje de \_ superposición de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="ab767-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="ab767-107">El mensaje de **\_ \_ \_ superposición de conjunto de Cap de WM** habilita o deshabilita el modo de superposición.</span><span class="sxs-lookup"><span data-stu-id="ab767-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="ab767-108">En el modo de superposición, el vídeo se muestra mediante la superposición de hardware.</span><span class="sxs-lookup"><span data-stu-id="ab767-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="ab767-109">Puede enviar este mensaje explícitamente o mediante la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .</span><span class="sxs-lookup"><span data-stu-id="ab767-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ab767-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab767-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab767-111"><span id="f"></span><span id="F"></span>*formato*</span><span class="sxs-lookup"><span data-stu-id="ab767-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="ab767-112">Marca de superposición.</span><span class="sxs-lookup"><span data-stu-id="ab767-112">Overlay flag.</span></span> <span data-ttu-id="ab767-113">Especifique **true** para este parámetro para habilitar el modo de superposición o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="ab767-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab767-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab767-114">Return Value</span></span>

<span data-ttu-id="ab767-115">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ab767-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab767-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab767-116">Remarks</span></span>

<span data-ttu-id="ab767-117">El uso de una superposición no requiere recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="ab767-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="ab767-118">El miembro **fHasOverlay** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica si el dispositivo es capaz de superponerse.</span><span class="sxs-lookup"><span data-stu-id="ab767-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="ab767-119">El miembro **fOverlayWindow** de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de superposición está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ab767-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="ab767-120">Al habilitar el modo de superposición, se deshabilita automáticamente el modo vista previa.</span><span class="sxs-lookup"><span data-stu-id="ab767-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab767-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab767-121">Requirements</span></span>



| <span data-ttu-id="ab767-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab767-122">Requirement</span></span> | <span data-ttu-id="ab767-123">Value</span><span class="sxs-lookup"><span data-stu-id="ab767-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab767-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab767-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab767-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab767-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab767-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab767-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab767-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab767-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab767-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab767-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab767-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab767-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab767-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab767-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab767-131">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ab767-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ab767-132">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ab767-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





