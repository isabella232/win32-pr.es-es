---
title: Mensaje de WM_CAP_EDIT_COPY (VFW. h)
description: El \_ \_ mensaje de copia de edición de Cap de WM \_ copia el contenido del búfer de trama de vídeo y la paleta asociada en el portapapeles. Puede enviar este mensaje explícitamente o mediante la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- Mensaje de WM_CAP_EDIT_COPY de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150626"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="0a9c2-105">\_Mensaje de \_ copia de edición de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="0a9c2-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="0a9c2-106">El mensaje de copia de edición de Cap de WM copia el contenido del búfer de trama de vídeo y la paleta asociada en el portapapeles. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a9c2-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="0a9c2-107">Puede enviar este mensaje explícitamente o mediante la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .</span><span class="sxs-lookup"><span data-stu-id="0a9c2-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="0a9c2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a9c2-108">Return Value</span></span>

<span data-ttu-id="0a9c2-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a9c2-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9c2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a9c2-110">Requirements</span></span>



| <span data-ttu-id="0a9c2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a9c2-111">Requirement</span></span> | <span data-ttu-id="0a9c2-112">Value</span><span class="sxs-lookup"><span data-stu-id="0a9c2-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0a9c2-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9c2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9c2-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a9c2-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0a9c2-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9c2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9c2-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a9c2-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a9c2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a9c2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a9c2-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a9c2-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9c2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a9c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9c2-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a9c2-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0a9c2-121">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a9c2-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





