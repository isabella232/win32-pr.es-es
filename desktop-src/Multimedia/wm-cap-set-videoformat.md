---
title: Mensaje de WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: El \_ \_ \_ mensaje de videoformat del conjunto de Cap de WM establece el formato de los datos de vídeo capturados. Puede enviar este mensaje explícitamente o mediante la macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- Mensaje de WM_CAP_SET_VIDEOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997057"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="3f0b1-105">\_Mensaje de \_ videoformat del conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="3f0b1-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="3f0b1-106">El mensaje de **\_ \_ \_ videoformat del conjunto de Cap de WM** establece el formato de los datos de vídeo capturados.</span><span class="sxs-lookup"><span data-stu-id="3f0b1-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="3f0b1-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="3f0b1-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="3f0b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f0b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0b1-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="3f0b1-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="3f0b1-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="3f0b1-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b1-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="3f0b1-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="3f0b1-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="3f0b1-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0b1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f0b1-113">Return Value</span></span>

<span data-ttu-id="3f0b1-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3f0b1-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f0b1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f0b1-115">Remarks</span></span>

<span data-ttu-id="3f0b1-116">Dado que los formatos de vídeo son específicos del dispositivo, las aplicaciones deben comprobar el valor devuelto de esta función para determinar si el controlador acepta el formato.</span><span class="sxs-lookup"><span data-stu-id="3f0b1-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f0b1-117">Requirements</span></span>



| <span data-ttu-id="3f0b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0b1-118">Requirement</span></span> | <span data-ttu-id="3f0b1-119">Value</span><span class="sxs-lookup"><span data-stu-id="3f0b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3f0b1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f0b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f0b1-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3f0b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3f0b1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f0b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f0b1-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f0b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f0b1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f0b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f0b1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0b1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f0b1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f0b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0b1-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3f0b1-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3f0b1-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3f0b1-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

