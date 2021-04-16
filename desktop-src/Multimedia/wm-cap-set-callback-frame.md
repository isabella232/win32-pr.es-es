---
title: Mensaje de WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: El \_ mensaje del \_ marco de \_ devolución de llamada del conjunto de Cap de WM \_ establece una función de devolución de llamada de vista previa en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura captura los fotogramas de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_FRAME de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676793"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="9ecde-106">\_Mensaje de \_ marco de devolución de llamada del conjunto de Cap de WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ecde-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="9ecde-107">El mensaje del **\_ marco de devolución de \_ \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada de vista previa en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ecde-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="9ecde-108">AVICap llama a este procedimiento cuando la ventana de captura captura los fotogramas de vista previa.</span><span class="sxs-lookup"><span data-stu-id="9ecde-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="9ecde-109">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="9ecde-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="9ecde-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ecde-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ecde-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="9ecde-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="9ecde-112">Puntero a la función de devolución de llamada de vista previa, de tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="9ecde-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="9ecde-113">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="9ecde-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ecde-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ecde-114">Return Value</span></span>

<span data-ttu-id="9ecde-115">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="9ecde-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ecde-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ecde-116">Remarks</span></span>

<span data-ttu-id="9ecde-117">La ventana captura llama a la función de devolución de llamada antes de mostrar los marcos de vista previa.</span><span class="sxs-lookup"><span data-stu-id="9ecde-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="9ecde-118">Esto permite que una aplicación modifique el marco si se desea.</span><span class="sxs-lookup"><span data-stu-id="9ecde-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="9ecde-119">Esta función de devolución de llamada no se utiliza durante la captura de vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="9ecde-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ecde-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ecde-120">Requirements</span></span>



| <span data-ttu-id="9ecde-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ecde-121">Requirement</span></span> | <span data-ttu-id="9ecde-122">Value</span><span class="sxs-lookup"><span data-stu-id="9ecde-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ecde-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecde-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecde-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ecde-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ecde-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecde-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecde-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ecde-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ecde-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ecde-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecde-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ecde-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ecde-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ecde-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecde-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ecde-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9ecde-131">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ecde-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





