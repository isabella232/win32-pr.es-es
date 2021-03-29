---
title: Mensaje de WM_CAP_PAL_AUTOCREATE (VFW. h)
description: El \_ mensaje de creación automática de Cap de WM Cap \_ \_ solicita que el vídeo de ejemplo del controlador de captura muestre fotogramas y cree automáticamente una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- Mensaje de WM_CAP_PAL_AUTOCREATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665957"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="28399-105">Mensaje de creación de la \_ PAL de Cap de WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="28399-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="28399-106">El mensaje de creación automática de **Cap de WM \_ Cap \_ \_** solicita que el vídeo de ejemplo del controlador de captura muestre fotogramas y cree automáticamente una nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="28399-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="28399-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .</span><span class="sxs-lookup"><span data-stu-id="28399-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="28399-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28399-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28399-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="28399-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="28399-110">Número de fotogramas que se van a muestrear.</span><span class="sxs-lookup"><span data-stu-id="28399-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="28399-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="28399-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="28399-112">Número de colores de la paleta.</span><span class="sxs-lookup"><span data-stu-id="28399-112">Number of colors in the palette.</span></span> <span data-ttu-id="28399-113">El valor máximo de este parámetro es 256.</span><span class="sxs-lookup"><span data-stu-id="28399-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28399-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28399-114">Return Value</span></span>

<span data-ttu-id="28399-115">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="28399-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="28399-116">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="28399-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="28399-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28399-117">Remarks</span></span>

<span data-ttu-id="28399-118">La secuencia de vídeo muestreada debe incluir todos los colores que desee en la paleta.</span><span class="sxs-lookup"><span data-stu-id="28399-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="28399-119">Para obtener la mejor paleta, puede que tenga que mostrar la secuencia completa en lugar de una parte de ella.</span><span class="sxs-lookup"><span data-stu-id="28399-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="28399-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28399-120">Requirements</span></span>



| <span data-ttu-id="28399-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28399-121">Requirement</span></span> | <span data-ttu-id="28399-122">Value</span><span class="sxs-lookup"><span data-stu-id="28399-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28399-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28399-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28399-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28399-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="28399-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28399-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28399-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28399-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28399-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28399-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28399-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="28399-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28399-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="28399-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28399-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="28399-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="28399-131">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="28399-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





