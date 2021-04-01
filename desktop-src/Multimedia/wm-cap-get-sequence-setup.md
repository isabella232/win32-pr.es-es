---
title: Mensaje de WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: El \_ \_ \_ \_ mensaje de configuración de la secuencia de obtención de Cap de WM recupera la configuración actual de los parámetros de captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- Mensaje de WM_CAP_GET_SEQUENCE_SETUP de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995909"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="b20fc-105">\_Mensaje de \_ configuración de secuencia de obtención de Cap de \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="b20fc-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="b20fc-106">El mensaje de configuración de la secuencia de obtención de Cap de WM recupera la configuración actual de los parámetros de captura de streaming. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b20fc-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="b20fc-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .</span><span class="sxs-lookup"><span data-stu-id="b20fc-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="b20fc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b20fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20fc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="b20fc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="b20fc-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="b20fc-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="b20fc-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="b20fc-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="b20fc-112">Puntero a una estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="b20fc-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20fc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b20fc-113">Return Value</span></span>

<span data-ttu-id="b20fc-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b20fc-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b20fc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b20fc-115">Remarks</span></span>

<span data-ttu-id="b20fc-116">Para obtener información sobre los parámetros que se usan para controlar la captura de streaming, consulte la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="b20fc-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20fc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b20fc-117">Requirements</span></span>



| <span data-ttu-id="b20fc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20fc-118">Requirement</span></span> | <span data-ttu-id="b20fc-119">Value</span><span class="sxs-lookup"><span data-stu-id="b20fc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b20fc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b20fc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b20fc-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b20fc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b20fc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b20fc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b20fc-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b20fc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b20fc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b20fc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b20fc-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b20fc-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20fc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b20fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20fc-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b20fc-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b20fc-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b20fc-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





