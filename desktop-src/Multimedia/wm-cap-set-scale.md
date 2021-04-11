---
title: Mensaje de WM_CAP_SET_SCALE (VFW. h)
description: El \_ \_ \_ mensaje de escala del límite de Cap de WM habilita o deshabilita el escalado de las imágenes de vídeo de vista previa.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- Mensaje de WM_CAP_SET_SCALE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151096"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="41ebc-104">\_Mensaje de \_ escala de conjunto de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="41ebc-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="41ebc-105">El mensaje de **\_ \_ \_ escala del límite de Cap de WM** habilita o deshabilita el escalado de las imágenes de vídeo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="41ebc-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="41ebc-106">Si el escalado está habilitado, el fotograma de vídeo capturado se ajusta a las dimensiones de la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="41ebc-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="41ebc-107">Puede enviar este mensaje explícitamente o mediante la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .</span><span class="sxs-lookup"><span data-stu-id="41ebc-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="41ebc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41ebc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ebc-109"><span id="f"></span><span id="F"></span>*formato*</span><span class="sxs-lookup"><span data-stu-id="41ebc-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="41ebc-110">Marca de escala de vista previa.</span><span class="sxs-lookup"><span data-stu-id="41ebc-110">Preview scaling flag.</span></span> <span data-ttu-id="41ebc-111">Especifique **true** para que este parámetro Estire los fotogramas de vista previa hasta el tamaño de la ventana de captura o **false** para mostrarlos en su tamaño natural.</span><span class="sxs-lookup"><span data-stu-id="41ebc-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ebc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41ebc-112">Return Value</span></span>

<span data-ttu-id="41ebc-113">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="41ebc-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ebc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41ebc-114">Remarks</span></span>

<span data-ttu-id="41ebc-115">Escalar imágenes de vista previa controla la presentación inmediata de los fotogramas capturados en la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="41ebc-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="41ebc-116">No tiene ningún efecto en el tamaño de los fotogramas guardados en el archivo.</span><span class="sxs-lookup"><span data-stu-id="41ebc-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="41ebc-117">El escalado no tiene ningún efecto cuando se usa la superposición para mostrar el vídeo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="41ebc-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ebc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ebc-118">Requirements</span></span>



| <span data-ttu-id="41ebc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ebc-119">Requirement</span></span> | <span data-ttu-id="41ebc-120">Value</span><span class="sxs-lookup"><span data-stu-id="41ebc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="41ebc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41ebc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41ebc-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41ebc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="41ebc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41ebc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41ebc-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41ebc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41ebc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41ebc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41ebc-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="41ebc-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ebc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="41ebc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ebc-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="41ebc-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="41ebc-129">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="41ebc-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





