---
title: Mensaje de WM_CAP_DRIVER_CONNECT (VFW. h)
description: El \_ mensaje de conexión del controlador Cap de WM \_ \_ conecta una ventana de captura a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- Mensaje de WM_CAP_DRIVER_CONNECT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422219"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="75cdf-105">\_Mensaje de \_ conexión del controlador Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="75cdf-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="75cdf-106">El mensaje de **\_ \_ \_ conexión del controlador Cap de WM** conecta una ventana de captura a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="75cdf-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="75cdf-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .</span><span class="sxs-lookup"><span data-stu-id="75cdf-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="75cdf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75cdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75cdf-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="75cdf-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="75cdf-110">Índice del controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="75cdf-110">Index of the capture driver.</span></span> <span data-ttu-id="75cdf-111">El índice puede oscilar entre 0 y 9.</span><span class="sxs-lookup"><span data-stu-id="75cdf-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75cdf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75cdf-112">Return Value</span></span>

<span data-ttu-id="75cdf-113">Devuelve **true** si es correcto o **false** si el controlador de captura especificado no se puede conectar a la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="75cdf-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="75cdf-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75cdf-114">Remarks</span></span>

<span data-ttu-id="75cdf-115">Al conectar un controlador de captura a una ventana de captura, se desconecta automáticamente cualquier controlador de captura conectado previamente.</span><span class="sxs-lookup"><span data-stu-id="75cdf-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="75cdf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75cdf-116">Requirements</span></span>



| <span data-ttu-id="75cdf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75cdf-117">Requirement</span></span> | <span data-ttu-id="75cdf-118">Value</span><span class="sxs-lookup"><span data-stu-id="75cdf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75cdf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75cdf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75cdf-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="75cdf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="75cdf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75cdf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75cdf-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75cdf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="75cdf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75cdf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75cdf-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="75cdf-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75cdf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="75cdf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75cdf-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="75cdf-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="75cdf-127">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="75cdf-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





