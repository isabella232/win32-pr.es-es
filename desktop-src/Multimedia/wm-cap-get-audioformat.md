---
title: Mensaje de WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: El \_ mensaje Cap \_ \_ AUDIOFORMAT de WM obtiene el formato de audio o el tamaño del formato de audio. Puede enviar este mensaje explícitamente o mediante las macros capGetAudioFormat y capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- Mensaje de WM_CAP_GET_AUDIOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421907"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="67765-105">\_Mensaje Cap \_ Get \_ AUDIOFORMAT de WM</span><span class="sxs-lookup"><span data-stu-id="67765-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="67765-106">El **mensaje \_ Cap \_ \_ AUDIOFORMAT de WM** obtiene el formato de audio o el tamaño del formato de audio.</span><span class="sxs-lookup"><span data-stu-id="67765-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="67765-107">Puede enviar este mensaje explícitamente o mediante las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .</span><span class="sxs-lookup"><span data-stu-id="67765-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="67765-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67765-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67765-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="67765-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="67765-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="67765-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="67765-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="67765-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="67765-112">Puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o **null**.</span><span class="sxs-lookup"><span data-stu-id="67765-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="67765-113">Si el valor es **null**, se devuelve el tamaño, en bytes, necesario para contener la estructura.</span><span class="sxs-lookup"><span data-stu-id="67765-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67765-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67765-114">Return Value</span></span>

<span data-ttu-id="67765-115">Devuelve el tamaño, en bytes, del formato de audio.</span><span class="sxs-lookup"><span data-stu-id="67765-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="67765-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67765-116">Remarks</span></span>

<span data-ttu-id="67765-117">Dado que los formatos de audio comprimidos varían en cuanto a los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar la memoria y, por último, solicitar los datos del formato de audio.</span><span class="sxs-lookup"><span data-stu-id="67765-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="67765-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67765-118">Requirements</span></span>



| <span data-ttu-id="67765-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67765-119">Requirement</span></span> | <span data-ttu-id="67765-120">Value</span><span class="sxs-lookup"><span data-stu-id="67765-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67765-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67765-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67765-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67765-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="67765-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67765-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67765-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67765-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67765-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67765-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67765-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="67765-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67765-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="67765-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67765-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="67765-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="67765-129">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="67765-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

