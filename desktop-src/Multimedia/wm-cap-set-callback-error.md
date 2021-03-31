---
title: Mensaje de WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: El \_ \_ \_ \_ mensaje de error de devolución de llamada de Cap de WM establece una función de devolución de llamada de error en la aplicación cliente. AVICap llama a este procedimiento cuando se producen errores. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_ERROR de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491140"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="3257c-106">\_Mensaje de \_ \_ error de devolución de llamada de límite de WM \_</span><span class="sxs-lookup"><span data-stu-id="3257c-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="3257c-107">El mensaje de **\_ error de devolución de \_ \_ llamada \_ de Cap de WM** establece una función de devolución de llamada de error en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3257c-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="3257c-108">AVICap llama a este procedimiento cuando se producen errores.</span><span class="sxs-lookup"><span data-stu-id="3257c-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="3257c-109">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="3257c-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="3257c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3257c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3257c-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="3257c-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="3257c-112">Puntero a la función de devolución de llamada de error, de tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span><span class="sxs-lookup"><span data-stu-id="3257c-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="3257c-113">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de error instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="3257c-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3257c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3257c-114">Return Value</span></span>

<span data-ttu-id="3257c-115">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="3257c-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="3257c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3257c-116">Remarks</span></span>

<span data-ttu-id="3257c-117">Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="3257c-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="3257c-118">Si se establece, AVICap llama al procedimiento de error en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="3257c-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="3257c-119">El disco está lleno.</span><span class="sxs-lookup"><span data-stu-id="3257c-119">The disk is full.</span></span>
-   <span data-ttu-id="3257c-120">No se puede conectar una ventana de captura con un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="3257c-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="3257c-121">No se puede abrir un dispositivo de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="3257c-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="3257c-122">El número de fotogramas descartados durante la captura supera el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="3257c-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="3257c-123">Los fotogramas no se pueden capturar debido a problemas de interrupción de sincronización verticales.</span><span class="sxs-lookup"><span data-stu-id="3257c-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="3257c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3257c-124">Requirements</span></span>



| <span data-ttu-id="3257c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3257c-125">Requirement</span></span> | <span data-ttu-id="3257c-126">Value</span><span class="sxs-lookup"><span data-stu-id="3257c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3257c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3257c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3257c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3257c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3257c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3257c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3257c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3257c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3257c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3257c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3257c-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3257c-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3257c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3257c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3257c-134">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3257c-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3257c-135">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3257c-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





