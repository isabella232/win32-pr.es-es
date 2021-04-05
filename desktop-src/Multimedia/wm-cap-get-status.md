---
title: Mensaje de WM_CAP_GET_STATUS (VFW. h)
description: El \_ \_ \_ mensaje de estado de Cap de WM Get recupera el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Mensaje de WM_CAP_GET_STATUS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078834"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="02a72-105">\_Mensaje de \_ Estado de obtención de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="02a72-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="02a72-106">El mensaje de **Estado de Cap de WM \_ \_ \_ Get** recupera el estado de la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="02a72-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="02a72-107">Puede enviar este mensaje explícitamente o mediante la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .</span><span class="sxs-lookup"><span data-stu-id="02a72-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="02a72-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02a72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a72-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="02a72-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="02a72-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="02a72-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="02a72-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="02a72-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="02a72-112">Puntero a una estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="02a72-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a72-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02a72-113">Return Value</span></span>

<span data-ttu-id="02a72-114">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="02a72-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a72-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a72-115">Remarks</span></span>

<span data-ttu-id="02a72-116">La estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contiene el estado actual de la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="02a72-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="02a72-117">Dado que este estado es dinámico y cambia en respuesta a varios mensajes, la aplicación debe inicializar esta estructura después de enviar el mensaje de [**\_ \_ \_ videoformat de Cap Cap de WM**](wm-cap-dlg-videoformat.md) (o mediante la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) y siempre que necesite habilitar elementos de menú o determinar el estado real de la ventana.</span><span class="sxs-lookup"><span data-stu-id="02a72-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a72-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02a72-118">Requirements</span></span>



| <span data-ttu-id="02a72-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a72-119">Requirement</span></span> | <span data-ttu-id="02a72-120">Value</span><span class="sxs-lookup"><span data-stu-id="02a72-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="02a72-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02a72-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="02a72-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="02a72-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02a72-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02a72-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="02a72-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02a72-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a72-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a72-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a72-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a72-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="02a72-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="02a72-129">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="02a72-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





