---
title: Mensaje de WM_CAP_SET_MCI_DEVICE (VFW. h)
description: El \_ mensaje del \_ dispositivo MCI del conjunto de Cap de WM \_ \_ especifica el nombre del dispositivo de vídeo MCI que se va a usar para capturar los datos. Puede enviar este mensaje explícitamente o mediante la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Mensaje de WM_CAP_SET_MCI_DEVICE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801190"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="5bd41-105">\_Mensaje de \_ \_ dispositivo MCI de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="5bd41-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="5bd41-106">El mensaje del **\_ \_ \_ \_ dispositivo MCI del conjunto de Cap de WM** especifica el nombre del dispositivo de vídeo MCI que se va a usar para capturar los datos.</span><span class="sxs-lookup"><span data-stu-id="5bd41-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="5bd41-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="5bd41-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="5bd41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bd41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd41-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="5bd41-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="5bd41-110">Puntero a una cadena terminada en null que contiene el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bd41-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd41-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bd41-111">Return Value</span></span>

<span data-ttu-id="5bd41-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5bd41-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd41-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bd41-113">Remarks</span></span>

<span data-ttu-id="5bd41-114">Este mensaje almacena el nombre del dispositivo MCI en una estructura interna.</span><span class="sxs-lookup"><span data-stu-id="5bd41-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="5bd41-115">No abre ni accede al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bd41-115">It does not open or access the device.</span></span> <span data-ttu-id="5bd41-116">El nombre de dispositivo predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="5bd41-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd41-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bd41-117">Requirements</span></span>



| <span data-ttu-id="5bd41-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd41-118">Requirement</span></span> | <span data-ttu-id="5bd41-119">Value</span><span class="sxs-lookup"><span data-stu-id="5bd41-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5bd41-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bd41-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd41-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bd41-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5bd41-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bd41-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd41-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bd41-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5bd41-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bd41-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd41-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bd41-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd41-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bd41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd41-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bd41-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5bd41-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bd41-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





