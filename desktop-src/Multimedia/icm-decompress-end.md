---
title: Mensaje de ICM_DECOMPRESS_END (VFW. h)
description: El mensaje final de descompresión de ICM \_ \_ notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- Mensaje de ICM_DECOMPRESS_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803379"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="29ed6-105">Descomprime el \_ \_ mensaje final de ICM</span><span class="sxs-lookup"><span data-stu-id="29ed6-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="29ed6-106">El **mensaje \_ \_ final** de descompresión de ICM notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión.</span><span class="sxs-lookup"><span data-stu-id="29ed6-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="29ed6-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="29ed6-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="29ed6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29ed6-108">Return Value</span></span>

<span data-ttu-id="29ed6-109">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="29ed6-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="29ed6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29ed6-110">Remarks</span></span>

<span data-ttu-id="29ed6-111">El controlador debe liberar todos los recursos asignados para el mensaje de [**\_ \_ Inicio de descomprimir ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="29ed6-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="29ed6-112">[**ICM \_ La instrucción DESCOMPRIMIr \_ Begin**](icm-decompress-begin.md) y **ICM \_ uncompre \_ End** no se anidan.</span><span class="sxs-lookup"><span data-stu-id="29ed6-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="29ed6-113">Si el controlador recibe **el \_ \_ Inicio** de la descompresión ICM antes de que se detenga la descompresión con el **\_ \_ fin de descomprimir ICM**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="29ed6-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ed6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29ed6-114">Requirements</span></span>



| <span data-ttu-id="29ed6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ed6-115">Requirement</span></span> | <span data-ttu-id="29ed6-116">Value</span><span class="sxs-lookup"><span data-stu-id="29ed6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="29ed6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29ed6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29ed6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="29ed6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="29ed6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29ed6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29ed6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29ed6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29ed6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29ed6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ed6-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ed6-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ed6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="29ed6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ed6-124">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="29ed6-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="29ed6-125">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="29ed6-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





