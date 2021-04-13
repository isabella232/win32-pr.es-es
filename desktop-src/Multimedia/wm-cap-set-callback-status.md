---
title: Mensaje de WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: El \_ \_ \_ \_ mensaje de estado de devolución de llamada de límite de Cap de WM establece una función de devolución de llamada de estado en la aplicación. AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_STATUS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489383"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="6b45a-106">\_Mensaje de \_ \_ Estado de devolución de llamada de límite de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="6b45a-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="6b45a-107">El mensaje de **\_ Estado de devolución de \_ \_ llamada \_ de límite de Cap de WM** establece una función de devolución de llamada de estado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b45a-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="6b45a-108">AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="6b45a-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="6b45a-109">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="6b45a-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="6b45a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b45a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b45a-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="6b45a-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="6b45a-112">Puntero a la función de devolución de llamada de estado, de tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="6b45a-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="6b45a-113">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de estado instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="6b45a-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b45a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b45a-114">Return Value</span></span>

<span data-ttu-id="6b45a-115">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="6b45a-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b45a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b45a-116">Remarks</span></span>

<span data-ttu-id="6b45a-117">Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="6b45a-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="6b45a-118">Si se establece, AVICap llama a este procedimiento en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="6b45a-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="6b45a-119">Se ha completado una sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="6b45a-119">A capture session is completed.</span></span>
-   <span data-ttu-id="6b45a-120">Un controlador de captura se conectó correctamente a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="6b45a-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="6b45a-121">Se crea una paleta óptima.</span><span class="sxs-lookup"><span data-stu-id="6b45a-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="6b45a-122">Se registra el número de fotogramas capturados.</span><span class="sxs-lookup"><span data-stu-id="6b45a-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b45a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b45a-123">Requirements</span></span>



| <span data-ttu-id="6b45a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b45a-124">Requirement</span></span> | <span data-ttu-id="6b45a-125">Value</span><span class="sxs-lookup"><span data-stu-id="6b45a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b45a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b45a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6b45a-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6b45a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b45a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b45a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6b45a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b45a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b45a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b45a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b45a-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b45a-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b45a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b45a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b45a-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b45a-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6b45a-134">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b45a-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





