---
title: Mensaje de WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: El \_ \_ \_ mensaje de Yield devoluciones de llamada del límite \_ de WM establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura produce durante la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_YIELD de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676567"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="12ec8-106">\_Mensaje de \_ \_ yield devoluciones de llamada de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="12ec8-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="12ec8-107">El mensaje de **\_ \_ \_ \_ yield devoluciones de llamada del límite de WM** establece una función de devolución de llamada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12ec8-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="12ec8-108">AVICap llama a este procedimiento cuando la ventana de captura produce durante la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="12ec8-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="12ec8-109">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="12ec8-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="12ec8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12ec8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ec8-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="12ec8-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="12ec8-112">Puntero a la función de devolución de llamada Yield, de tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="12ec8-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="12ec8-113">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada yield instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="12ec8-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ec8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12ec8-114">Return Value</span></span>

<span data-ttu-id="12ec8-115">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="12ec8-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="12ec8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12ec8-116">Remarks</span></span>

<span data-ttu-id="12ec8-117">Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada yield.</span><span class="sxs-lookup"><span data-stu-id="12ec8-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="12ec8-118">Se llama a la función de devolución de llamada yield al menos una vez para cada fotograma de vídeo capturado durante la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="12ec8-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="12ec8-119">Si se instala una función de devolución de llamada Yield, se llamará independientemente del estado del miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="12ec8-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="12ec8-120">Si se usa la función de devolución de llamada Yield, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión.</span><span class="sxs-lookup"><span data-stu-id="12ec8-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="12ec8-121">Se puede deshabilitar después de que finalice la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="12ec8-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="12ec8-122">Normalmente, las aplicaciones realizan algún tipo de procesamiento de mensajes en la función de devolución de llamada que consta de un bucle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , como en el bucle de mensajes de una función [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="12ec8-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="12ec8-123">La función de devolución de llamada yield también debe filtrar y quitar los mensajes que pueden provocar problemas de reentrada.</span><span class="sxs-lookup"><span data-stu-id="12ec8-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="12ec8-124">Normalmente, una aplicación devuelve **true** en el procedimiento Yield para continuar con la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="12ec8-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="12ec8-125">Si una función de devolución de llamada yield devuelve **false**, la ventana de captura detiene el proceso de captura.</span><span class="sxs-lookup"><span data-stu-id="12ec8-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ec8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ec8-126">Requirements</span></span>



| <span data-ttu-id="12ec8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ec8-127">Requirement</span></span> | <span data-ttu-id="12ec8-128">Value</span><span class="sxs-lookup"><span data-stu-id="12ec8-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12ec8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12ec8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12ec8-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12ec8-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12ec8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12ec8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12ec8-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12ec8-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12ec8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12ec8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ec8-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ec8-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ec8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="12ec8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ec8-136">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="12ec8-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="12ec8-137">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="12ec8-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

