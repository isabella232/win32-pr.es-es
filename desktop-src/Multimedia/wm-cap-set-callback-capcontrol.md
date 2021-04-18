---
title: Mensaje de WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: El \_ \_ \_ mensaje CAPCONTROL de devolución de llamada del conjunto de Cap \_ de WM establece una función de devolución de llamada en la aplicación, lo que le otorga un control de grabación preciso. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_CAPCONTROL de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666027"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="fc943-105">\_Mensaje de \_ \_ CAPCONTROL de devolución de llamada de límite de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="fc943-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="fc943-106">El **mensaje \_ CAPCONTROL de \_ devolución de \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada en la aplicación, lo que le otorga un control de grabación preciso.</span><span class="sxs-lookup"><span data-stu-id="fc943-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="fc943-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="fc943-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="fc943-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc943-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="fc943-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="fc943-110">Puntero a la función de devolución de llamada, de tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="fc943-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="fc943-111">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="fc943-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc943-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc943-112">Return Value</span></span>

<span data-ttu-id="fc943-113">Devuelve **true** si es correcto o **false** si una captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="fc943-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc943-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc943-114">Remarks</span></span>

<span data-ttu-id="fc943-115">Se utiliza una función de devolución de llamada única para proporcionar a la aplicación un control preciso sobre los momentos en que se inicia y finaliza la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="fc943-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="fc943-116">En primer lugar, la ventana de captura llama al procedimiento con *nState* establecido en CONTROLCALLBACK \_ preroll una vez que se han asignado todos los búferes y se han completado todos los demás preparados de captura.</span><span class="sxs-lookup"><span data-stu-id="fc943-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="fc943-117">Esto proporciona a la aplicación la capacidad de revertir los orígenes de vídeo y volver de la función de devolución de llamada en el momento en que se inicia la grabación.</span><span class="sxs-lookup"><span data-stu-id="fc943-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="fc943-118">Un valor devuelto de **true** desde la función de devolución de llamada continúa la captura y un valor devuelto de **false** anula la captura.</span><span class="sxs-lookup"><span data-stu-id="fc943-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="fc943-119">Una vez iniciada la captura, se llama a esta función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK \_ para permitir que la aplicación finalice la captura devolviendo **false**.</span><span class="sxs-lookup"><span data-stu-id="fc943-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc943-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc943-120">Requirements</span></span>



| <span data-ttu-id="fc943-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc943-121">Requirement</span></span> | <span data-ttu-id="fc943-122">Value</span><span class="sxs-lookup"><span data-stu-id="fc943-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fc943-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc943-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fc943-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc943-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fc943-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc943-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fc943-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc943-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc943-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc943-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc943-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc943-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc943-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc943-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc943-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fc943-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fc943-131">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fc943-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





