---
title: Mensaje de ICM_COMPRESS_END (VFW. h)
description: El mensaje de finalización de compresión ICM \_ \_ notifica a un controlador de compresión de vídeo que finalice la compresión y libere los recursos asignados para la compresión. Puede enviar este mensaje explícitamente o mediante la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Mensaje de ICM_COMPRESS_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489899"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="569ab-105">\_Mensaje final de compresión ICM \_</span><span class="sxs-lookup"><span data-stu-id="569ab-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="569ab-106">El mensaje de **\_ \_ finalización** de compresión ICM notifica a un controlador de compresión de vídeo que finalice la compresión y libere los recursos asignados para la compresión.</span><span class="sxs-lookup"><span data-stu-id="569ab-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="569ab-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .</span><span class="sxs-lookup"><span data-stu-id="569ab-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="569ab-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="569ab-108">Return Value</span></span>

<span data-ttu-id="569ab-109">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="569ab-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="569ab-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="569ab-110">Remarks</span></span>

<span data-ttu-id="569ab-111">VCM guarda la configuración del mensaje de [**Inicio de \_ compresión \_ ICM**](icm-compress-begin.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="569ab-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="569ab-112">**ICM \_ Los \_** **\_ \_ extremos** de la compresión Begin y ICM no se anidan.</span><span class="sxs-lookup"><span data-stu-id="569ab-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="569ab-113">Si el controlador recibe la compresión de **ICM \_ \_ comienza** antes de que se detenga la compresión con el **\_ \_ fin de comprimir ICM**, debe reiniciar la compresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="569ab-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="569ab-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="569ab-114">Requirements</span></span>



| <span data-ttu-id="569ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="569ab-115">Requirement</span></span> | <span data-ttu-id="569ab-116">Value</span><span class="sxs-lookup"><span data-stu-id="569ab-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="569ab-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="569ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="569ab-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="569ab-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="569ab-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="569ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="569ab-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="569ab-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="569ab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="569ab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="569ab-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="569ab-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="569ab-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="569ab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569ab-124">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="569ab-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="569ab-125">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="569ab-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





