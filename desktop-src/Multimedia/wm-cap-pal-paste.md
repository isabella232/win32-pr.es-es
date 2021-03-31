---
title: Mensaje de WM_CAP_PAL_PASTE (VFW. h)
description: El \_ \_ \_ mensaje de pegado PAL de Cap de WM copia la paleta del portapapeles y la pasa a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- Mensaje de WM_CAP_PAL_PASTE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996191"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="71093-105">\_Mensaje de \_ pegado PAL de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="71093-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="71093-106">El mensaje de **\_ \_ \_ pegado PAL de Cap de WM** copia la paleta del portapapeles y la pasa a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="71093-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="71093-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .</span><span class="sxs-lookup"><span data-stu-id="71093-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="71093-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71093-108">Return Value</span></span>

<span data-ttu-id="71093-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="71093-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="71093-110">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="71093-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="71093-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71093-111">Remarks</span></span>

<span data-ttu-id="71093-112">Un controlador de captura usa una paleta cuando lo requiere el formato de vídeo digitalizado especificado.</span><span class="sxs-lookup"><span data-stu-id="71093-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="71093-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71093-113">Requirements</span></span>



| <span data-ttu-id="71093-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="71093-114">Requirement</span></span> | <span data-ttu-id="71093-115">Value</span><span class="sxs-lookup"><span data-stu-id="71093-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="71093-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71093-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71093-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71093-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="71093-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71093-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71093-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71093-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71093-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71093-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71093-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="71093-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71093-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="71093-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71093-123">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="71093-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="71093-124">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="71093-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





