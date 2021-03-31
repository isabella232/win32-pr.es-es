---
title: Mensaje de WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: El \_ mensaje Cap de WM \_ obtener \_ videoformat recupera una copia del formato de vídeo en uso o el tamaño necesario para el formato de vídeo. Puede enviar este mensaje explícitamente o mediante las macros capGetVideoFormat y capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- Mensaje de WM_CAP_GET_VIDEOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996359"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="26f67-105">\_Mensaje de \_ obtención de formato de Cap \_ de WM</span><span class="sxs-lookup"><span data-stu-id="26f67-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="26f67-106">El **mensaje \_ Cap de WM \_ obtener \_ videoformat** recupera una copia del formato de vídeo en uso o el tamaño necesario para el formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="26f67-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="26f67-107">Puede enviar este mensaje explícitamente o mediante las macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) y [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .</span><span class="sxs-lookup"><span data-stu-id="26f67-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="26f67-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f67-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="26f67-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="26f67-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="26f67-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="26f67-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="26f67-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="26f67-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="26f67-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="26f67-113">También puede especificar **null** para recuperar el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="26f67-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f67-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f67-114">Return Value</span></span>

<span data-ttu-id="26f67-115">Devuelve el tamaño, en bytes, del formato de vídeo o cero si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="26f67-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="26f67-116">En el caso de los formatos de vídeo que requieran una paleta, también se devuelve la paleta actual.</span><span class="sxs-lookup"><span data-stu-id="26f67-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f67-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26f67-117">Remarks</span></span>

<span data-ttu-id="26f67-118">Dado que los formatos de vídeo comprimidos varían en cuanto a los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar la memoria y, por último, solicitar los datos de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="26f67-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f67-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f67-119">Requirements</span></span>



| <span data-ttu-id="26f67-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f67-120">Requirement</span></span> | <span data-ttu-id="26f67-121">Value</span><span class="sxs-lookup"><span data-stu-id="26f67-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="26f67-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26f67-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26f67-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26f67-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26f67-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26f67-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26f67-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f67-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f67-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f67-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f67-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="26f67-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="26f67-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="26f67-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

