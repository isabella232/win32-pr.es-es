---
title: Mensaje de ICM_GETBUFFERSWANTED (VFW. h)
description: El \_ mensaje GETBUFFERSWANTED ICM consulta a un controlador el número de búferes que se van a asignar. Puede enviar este mensaje explícitamente o mediante la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- Mensaje de ICM_GETBUFFERSWANTED de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996053"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="e654c-105">\_Mensaje GETBUFFERSWANTED ICM</span><span class="sxs-lookup"><span data-stu-id="e654c-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="e654c-106">El **mensaje \_ GETBUFFERSWANTED ICM** consulta a un controlador el número de búferes que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="e654c-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="e654c-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .</span><span class="sxs-lookup"><span data-stu-id="e654c-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="e654c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e654c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e654c-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span><span class="sxs-lookup"><span data-stu-id="e654c-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="e654c-110">Address para contener el número de muestras que el controlador necesita para representar los datos de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="e654c-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e654c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e654c-111">Return Value</span></span>

<span data-ttu-id="e654c-112">Devuelve ICERR \_ OK si es correcto o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e654c-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e654c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e654c-113">Remarks</span></span>

<span data-ttu-id="e654c-114">Este mensaje lo usan los controladores que usan Hardware para representar datos y desean garantizar un retraso mínimo causado por la espera de que lleguen los búferes.</span><span class="sxs-lookup"><span data-stu-id="e654c-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="e654c-115">Por ejemplo, si un controlador controla una placa de descompresión de vídeo que puede contener 10 fotogramas de vídeo, podría devolver 10 para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e654c-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="e654c-116">Esto indica a las aplicaciones que intenten mantener 10 fotogramas por encima del marco que necesita actualmente.</span><span class="sxs-lookup"><span data-stu-id="e654c-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e654c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e654c-117">Requirements</span></span>



| <span data-ttu-id="e654c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e654c-118">Requirement</span></span> | <span data-ttu-id="e654c-119">Value</span><span class="sxs-lookup"><span data-stu-id="e654c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e654c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e654c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e654c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e654c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e654c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e654c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e654c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e654c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e654c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e654c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e654c-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e654c-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e654c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e654c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e654c-127">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e654c-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e654c-128">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e654c-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





