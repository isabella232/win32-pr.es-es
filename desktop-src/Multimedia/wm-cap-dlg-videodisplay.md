---
title: Mensaje de WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: El \_ \_ \_ mensaje de Videopresentación de Cap de salida de WM muestra un cuadro de diálogo en el que el usuario puede establecer o ajustar la salida de vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- Mensaje de WM_CAP_DLG_VIDEODISPLAY de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996360"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="62eeb-104">\_Mensaje de \_ vídeo de presentación de Cap \_ de WM</span><span class="sxs-lookup"><span data-stu-id="62eeb-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="62eeb-105">El mensaje de **\_ \_ \_ Videopresentación de Cap** de salida de WM muestra un cuadro de diálogo en el que el usuario puede establecer o ajustar la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62eeb-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="62eeb-106">Este cuadro de diálogo puede contener controles que afectan al matiz, al contraste y al brillo de la imagen mostrada, así como a la alineación del color de la clave.</span><span class="sxs-lookup"><span data-stu-id="62eeb-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="62eeb-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .</span><span class="sxs-lookup"><span data-stu-id="62eeb-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="62eeb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62eeb-108">Return Value</span></span>

<span data-ttu-id="62eeb-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="62eeb-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="62eeb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62eeb-110">Remarks</span></span>

<span data-ttu-id="62eeb-111">Los controles de este cuadro de diálogo no afectan a los datos de vídeo digitalizados; solo afectan a la salida o a la presentación de la señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62eeb-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="62eeb-112">El cuadro de diálogo presentación en vídeo es único para cada controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="62eeb-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="62eeb-113">Es posible que algunos controladores de captura no admitan un cuadro de diálogo de presentación en vídeo.</span><span class="sxs-lookup"><span data-stu-id="62eeb-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="62eeb-114">Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoDisplay** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="62eeb-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="62eeb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62eeb-115">Requirements</span></span>



| <span data-ttu-id="62eeb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62eeb-116">Requirement</span></span> | <span data-ttu-id="62eeb-117">Value</span><span class="sxs-lookup"><span data-stu-id="62eeb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62eeb-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62eeb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62eeb-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="62eeb-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="62eeb-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62eeb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62eeb-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="62eeb-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="62eeb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62eeb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62eeb-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="62eeb-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62eeb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="62eeb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62eeb-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="62eeb-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="62eeb-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="62eeb-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





