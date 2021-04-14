---
title: Mensaje de WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: El \_ mensaje del \_ controlador Cap de WM \_ obtener \_ Cap devuelve las capacidades de hardware del controlador de captura conectado actualmente a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- Mensaje de WM_CAP_DRIVER_GET_CAPS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535344"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="04b26-105">Mensaje de obtención Cap del \_ controlador Cap de WM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="04b26-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="04b26-106">El mensaje del **\_ controlador Cap de WM \_ \_ obtener \_ Cap** devuelve las capacidades de hardware del controlador de captura conectado actualmente a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="04b26-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="04b26-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .</span><span class="sxs-lookup"><span data-stu-id="04b26-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="04b26-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04b26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b26-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="04b26-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="04b26-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="04b26-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="04b26-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span><span class="sxs-lookup"><span data-stu-id="04b26-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="04b26-112">Puntero a la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) para que contenga las capacidades de hardware.</span><span class="sxs-lookup"><span data-stu-id="04b26-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04b26-113">Return Value</span></span>

<span data-ttu-id="04b26-114">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="04b26-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b26-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04b26-115">Remarks</span></span>

<span data-ttu-id="04b26-116">Las capacidades devueltas en [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) son constantes para un controlador de captura determinado.</span><span class="sxs-lookup"><span data-stu-id="04b26-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="04b26-117">Las aplicaciones necesitan recuperar esta información una vez cuando el controlador de captura se conecta por primera vez a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="04b26-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b26-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b26-118">Requirements</span></span>



| <span data-ttu-id="04b26-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b26-119">Requirement</span></span> | <span data-ttu-id="04b26-120">Value</span><span class="sxs-lookup"><span data-stu-id="04b26-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="04b26-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b26-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04b26-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04b26-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="04b26-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b26-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04b26-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04b26-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04b26-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04b26-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b26-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b26-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b26-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="04b26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b26-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="04b26-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="04b26-129">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="04b26-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





