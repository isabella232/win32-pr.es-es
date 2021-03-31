---
title: Mensaje de WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: El \_ mensaje de \_ vídeo de formato de Cap de WM Dlg \_ muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- Mensaje de WM_CAP_DLG_VIDEOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996267"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="b7f83-104">\_Mensaje de \_ \_ videoformateador de Cap de WM</span><span class="sxs-lookup"><span data-stu-id="b7f83-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="b7f83-105">El mensaje de vídeo de **formato de Cap de WM \_ \_ \_ Dlg** muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b7f83-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="b7f83-106">El cuadro de diálogo formato de vídeo se puede usar para seleccionar las opciones dimensiones de imagen, profundidad de bits y compresión de hardware.</span><span class="sxs-lookup"><span data-stu-id="b7f83-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="b7f83-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="b7f83-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="b7f83-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7f83-108">Return Value</span></span>

<span data-ttu-id="b7f83-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b7f83-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f83-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7f83-110">Remarks</span></span>

<span data-ttu-id="b7f83-111">Una vez que se devuelve este mensaje, es posible que las aplicaciones necesiten actualizar la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque el usuario podría haber cambiado las dimensiones de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b7f83-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="b7f83-112">El cuadro de diálogo formato de vídeo es único para cada controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="b7f83-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="b7f83-113">Es posible que algunos controladores de captura no admitan un cuadro de diálogo formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b7f83-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="b7f83-114">Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span><span class="sxs-lookup"><span data-stu-id="b7f83-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f83-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f83-115">Requirements</span></span>



| <span data-ttu-id="b7f83-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f83-116">Requirement</span></span> | <span data-ttu-id="b7f83-117">Value</span><span class="sxs-lookup"><span data-stu-id="b7f83-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7f83-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f83-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b7f83-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b7f83-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f83-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7f83-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b7f83-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7f83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f83-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7f83-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f83-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f83-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b7f83-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b7f83-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b7f83-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





