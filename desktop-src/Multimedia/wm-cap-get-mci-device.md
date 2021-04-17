---
title: Mensaje de WM_CAP_GET_MCI_DEVICE (VFW. h)
description: El \_ mensaje Cap \_ de WM Get \_ MCI \_ Device recupera el nombre de un dispositivo MCI previamente establecido con el \_ \_ mensaje de \_ dispositivo MCI del conjunto de Cap de WM \_ . Puede enviar este mensaje explícitamente o mediante la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- Mensaje de WM_CAP_GET_MCI_DEVICE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488963"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="0a17f-105">\_Mensaje de \_ \_ dispositivo MCI de obtención de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="0a17f-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="0a17f-106">El **mensaje \_ Cap de WM \_ Get \_ MCI \_ Device** recupera el nombre de un dispositivo MCI previamente establecido con el mensaje de [**\_ \_ \_ \_ dispositivo MCI del conjunto de Cap de WM**](wm-cap-set-mci-device.md) .</span><span class="sxs-lookup"><span data-stu-id="0a17f-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="0a17f-107">Puede enviar este mensaje explícitamente o mediante la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="0a17f-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="0a17f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a17f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a17f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="0a17f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="0a17f-110">Longitud, en bytes, del búfer al que se hace referencia en **szName**.</span><span class="sxs-lookup"><span data-stu-id="0a17f-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="0a17f-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="0a17f-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="0a17f-112">Puntero a una cadena terminada en null que contiene el nombre del dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0a17f-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a17f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a17f-113">Return Value</span></span>

<span data-ttu-id="0a17f-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a17f-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a17f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a17f-115">Requirements</span></span>



| <span data-ttu-id="0a17f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a17f-116">Requirement</span></span> | <span data-ttu-id="0a17f-117">Value</span><span class="sxs-lookup"><span data-stu-id="0a17f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0a17f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a17f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a17f-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a17f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0a17f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a17f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a17f-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a17f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a17f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a17f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a17f-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a17f-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a17f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a17f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a17f-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a17f-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0a17f-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a17f-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





