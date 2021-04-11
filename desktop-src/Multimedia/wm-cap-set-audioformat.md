---
title: Mensaje de WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: El \_ mensaje AUDIOFORMAT de Cap de WM \_ \_ establece el formato de audio que se va a usar al realizar la captura de flujo o paso. Puede enviar este mensaje explícitamente o mediante la macro capSetAudioFormat.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- Mensaje de WM_CAP_SET_AUDIOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150443"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="59c97-105">\_ \_ Mensaje AUDIOFORMAT de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="59c97-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="59c97-106">El **mensaje \_ \_ \_ AUDIOFORMAT de Cap de WM** establece el formato de audio que se va a usar al realizar la captura de flujo o paso.</span><span class="sxs-lookup"><span data-stu-id="59c97-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="59c97-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .</span><span class="sxs-lookup"><span data-stu-id="59c97-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="59c97-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59c97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c97-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="59c97-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="59c97-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="59c97-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="59c97-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="59c97-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="59c97-112">Puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) que define el formato de audio.</span><span class="sxs-lookup"><span data-stu-id="59c97-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c97-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59c97-113">Return Value</span></span>

<span data-ttu-id="59c97-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="59c97-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c97-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c97-115">Requirements</span></span>



| <span data-ttu-id="59c97-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c97-116">Requirement</span></span> | <span data-ttu-id="59c97-117">Value</span><span class="sxs-lookup"><span data-stu-id="59c97-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="59c97-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59c97-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59c97-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59c97-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="59c97-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59c97-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59c97-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59c97-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="59c97-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59c97-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c97-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c97-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c97-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="59c97-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c97-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="59c97-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="59c97-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="59c97-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

