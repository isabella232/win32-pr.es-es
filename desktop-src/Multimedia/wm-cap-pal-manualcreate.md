---
title: Mensaje de WM_CAP_PAL_MANUALCREATE (VFW. h)
description: El \_ mensaje MANUALCREATE Cap de WM Cap \_ \_ solicita que el controlador de captura muestre manualmente los fotogramas de vídeo y cree una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Mensaje de WM_CAP_PAL_MANUALCREATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801868"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="7aa55-105">\_ \_ Mensaje MANUALCREATE de PAL Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="7aa55-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="7aa55-106">El **mensaje \_ \_ \_ MANUALCREATE Cap de WM Cap** solicita que el controlador de captura muestre manualmente los fotogramas de vídeo y cree una nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="7aa55-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="7aa55-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .</span><span class="sxs-lookup"><span data-stu-id="7aa55-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="7aa55-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7aa55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa55-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span><span class="sxs-lookup"><span data-stu-id="7aa55-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="7aa55-110">Marca de histograma de la paleta.</span><span class="sxs-lookup"><span data-stu-id="7aa55-110">Palette histogram flag.</span></span> <span data-ttu-id="7aa55-111">Establezca este parámetro en **true** para cada marco incluido en la creación de la paleta óptima.</span><span class="sxs-lookup"><span data-stu-id="7aa55-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="7aa55-112">Después de recopilar el último fotograma, establezca este parámetro en **false** para calcular la paleta óptima y enviarlo al controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="7aa55-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="7aa55-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="7aa55-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="7aa55-114">Número de colores de la paleta.</span><span class="sxs-lookup"><span data-stu-id="7aa55-114">Number of colors in the palette.</span></span> <span data-ttu-id="7aa55-115">El valor máximo de este parámetro es 256.</span><span class="sxs-lookup"><span data-stu-id="7aa55-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="7aa55-116">Este valor solo se usa durante la recopilación del primer fotograma de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="7aa55-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa55-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7aa55-117">Return Value</span></span>

<span data-ttu-id="7aa55-118">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7aa55-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="7aa55-119">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="7aa55-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa55-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aa55-120">Requirements</span></span>



| <span data-ttu-id="7aa55-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa55-121">Requirement</span></span> | <span data-ttu-id="7aa55-122">Value</span><span class="sxs-lookup"><span data-stu-id="7aa55-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7aa55-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aa55-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa55-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7aa55-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7aa55-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aa55-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa55-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7aa55-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7aa55-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7aa55-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aa55-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa55-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aa55-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aa55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa55-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7aa55-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7aa55-131">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7aa55-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





