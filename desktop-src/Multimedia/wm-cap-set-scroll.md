---
title: Mensaje de WM_CAP_SET_SCROLL (VFW. h)
description: El \_ \_ mensaje de desplazamiento del conjunto de Cap de WM \_ define la parte del fotograma de vídeo que se va a mostrar en la ventana de captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Mensaje de WM_CAP_SET_SCROLL de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492946"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="209ec-104">\_Mensaje de \_ desplazamiento de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="209ec-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="209ec-105">El mensaje de desplazamiento del conjunto de Cap de WM define la parte del fotograma de vídeo que se va a mostrar en la ventana de captura. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="209ec-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="209ec-106">Este mensaje establece la esquina superior izquierda del área de cliente de la ventana de captura en las coordenadas de un píxel especificado dentro del fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="209ec-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="209ec-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="209ec-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="209ec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="209ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209ec-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span><span class="sxs-lookup"><span data-stu-id="209ec-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="209ec-110">Dirección que va a contener la posición de desplazamiento deseada.</span><span class="sxs-lookup"><span data-stu-id="209ec-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209ec-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="209ec-111">Return Value</span></span>

<span data-ttu-id="209ec-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="209ec-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="209ec-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="209ec-113">Remarks</span></span>

<span data-ttu-id="209ec-114">La posición de desplazamiento afecta a la imagen en los modos de vista previa y de superposición.</span><span class="sxs-lookup"><span data-stu-id="209ec-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="209ec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="209ec-115">Requirements</span></span>



| <span data-ttu-id="209ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="209ec-116">Requirement</span></span> | <span data-ttu-id="209ec-117">Value</span><span class="sxs-lookup"><span data-stu-id="209ec-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="209ec-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="209ec-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="209ec-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="209ec-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="209ec-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="209ec-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="209ec-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="209ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="209ec-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="209ec-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209ec-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="209ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209ec-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="209ec-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="209ec-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="209ec-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





