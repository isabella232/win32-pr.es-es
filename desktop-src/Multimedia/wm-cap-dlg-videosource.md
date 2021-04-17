---
title: Mensaje de WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: El \_ \_ \_ mensaje de videosource de Cap de WM Dlg muestra un cuadro de diálogo en el que el usuario puede controlar el origen de vídeo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- Mensaje de WM_CAP_DLG_VIDEOSOURCE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490114"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="9de39-104">\_Mensaje de \_ videosource de límite de WM Dlg \_</span><span class="sxs-lookup"><span data-stu-id="9de39-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="9de39-105">El mensaje de **\_ \_ \_ videosource de Cap de WM Dlg** muestra un cuadro de diálogo en el que el usuario puede controlar el origen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9de39-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="9de39-106">El cuadro de diálogo origen del vídeo puede contener controles que seleccionen orígenes de entrada; modificar el matiz, el contraste y el brillo de la imagen; y modifique la calidad del vídeo antes de digitalizar las imágenes en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9de39-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="9de39-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .</span><span class="sxs-lookup"><span data-stu-id="9de39-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9de39-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9de39-108">Return Value</span></span>

<span data-ttu-id="9de39-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9de39-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de39-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9de39-110">Remarks</span></span>

<span data-ttu-id="9de39-111">El cuadro de diálogo origen de vídeo es único para cada controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="9de39-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="9de39-112">Es posible que algunos controladores de captura no admitan un cuadro de diálogo origen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9de39-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="9de39-113">Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoSource** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="9de39-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9de39-114">Requirements</span></span>



| <span data-ttu-id="9de39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de39-115">Requirement</span></span> | <span data-ttu-id="9de39-116">Value</span><span class="sxs-lookup"><span data-stu-id="9de39-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9de39-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9de39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9de39-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9de39-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9de39-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9de39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9de39-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9de39-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9de39-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9de39-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de39-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de39-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de39-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9de39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de39-124">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9de39-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9de39-125">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9de39-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





