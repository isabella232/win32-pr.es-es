---
title: Mensaje de WM_CAP_ABORT (VFW. h)
description: El \_ mensaje de anulación de Cap de WM \_ detiene la operación de captura.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Mensaje de WM_CAP_ABORT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534108"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="1fcbb-104">\_Mensaje de anulación de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="1fcbb-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="1fcbb-105">El mensaje de **\_ \_ anulación de Cap de WM** detiene la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="1fcbb-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="1fcbb-106">En el caso de la captura de pasos, los datos de la imagen recopilados hasta el momento del mensaje de **\_ \_ anulación del Cap de WM** se conservarán en el archivo de captura, pero el audio no se capturará.</span><span class="sxs-lookup"><span data-stu-id="1fcbb-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="1fcbb-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .</span><span class="sxs-lookup"><span data-stu-id="1fcbb-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="1fcbb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fcbb-108">Return Value</span></span>

<span data-ttu-id="1fcbb-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1fcbb-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcbb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fcbb-110">Remarks</span></span>

<span data-ttu-id="1fcbb-111">La operación de captura debe proporcionar el uso de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1fcbb-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="1fcbb-112">Use el mensaje de [**\_ \_ detención de Cap de WM**](wm-cap-stop.md) para detener la captura de paso en la posición actual y, a continuación, capturar audio.</span><span class="sxs-lookup"><span data-stu-id="1fcbb-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcbb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcbb-113">Requirements</span></span>



| <span data-ttu-id="1fcbb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcbb-114">Requirement</span></span> | <span data-ttu-id="1fcbb-115">Value</span><span class="sxs-lookup"><span data-stu-id="1fcbb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1fcbb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcbb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcbb-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1fcbb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1fcbb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcbb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcbb-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fcbb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1fcbb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fcbb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcbb-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcbb-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcbb-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fcbb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcbb-123">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1fcbb-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1fcbb-124">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1fcbb-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





