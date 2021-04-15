---
title: Mensaje de WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: El \_ \_ \_ \_ mensaje WAVESTREAM de devolución de llamada del conjunto de Cap de WM establece una función de devolución de llamada en la aplicación.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_WAVESTREAM de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492947"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="b4956-104">\_Mensaje de \_ \_ error de devolución de llamada de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="b4956-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="b4956-105">El **mensaje \_ WAVESTREAM de \_ devolución de \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4956-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="b4956-106">AVICap llama a este procedimiento durante la captura de streaming cuando un nuevo búfer de audio está disponible.</span><span class="sxs-lookup"><span data-stu-id="b4956-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="b4956-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="b4956-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="b4956-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4956-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4956-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="b4956-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="b4956-110">Puntero a la función de devolución de llamada de flujo de onda, de tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="b4956-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="b4956-111">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de flujo de onda instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="b4956-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4956-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4956-112">Return Value</span></span>

<span data-ttu-id="b4956-113">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="b4956-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4956-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4956-114">Remarks</span></span>

<span data-ttu-id="b4956-115">La ventana captura llama al procedimiento antes de escribir el búfer de audio en el disco.</span><span class="sxs-lookup"><span data-stu-id="b4956-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="b4956-116">Esto permite que las aplicaciones modifiquen el búfer de audio si se desea.</span><span class="sxs-lookup"><span data-stu-id="b4956-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="b4956-117">Si se utiliza una función de devolución de llamada de flujo de onda, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión.</span><span class="sxs-lookup"><span data-stu-id="b4956-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="b4956-118">Se puede deshabilitar después de que finalice la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="b4956-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4956-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4956-119">Requirements</span></span>



| <span data-ttu-id="b4956-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4956-120">Requirement</span></span> | <span data-ttu-id="b4956-121">Value</span><span class="sxs-lookup"><span data-stu-id="b4956-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4956-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4956-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4956-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4956-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b4956-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4956-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4956-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4956-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4956-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4956-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4956-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4956-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4956-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4956-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4956-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4956-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b4956-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4956-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





