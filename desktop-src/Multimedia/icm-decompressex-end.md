---
title: Mensaje de ICM_DECOMPRESSEX_END (VFW. h)
description: El \_ mensaje de \_ finalización DECOMPRESSEX de ICM notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- Mensaje de ICM_DECOMPRESSEX_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535026"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="28dac-105">\_Mensaje final de DECOMPRESSEX ICM \_</span><span class="sxs-lookup"><span data-stu-id="28dac-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="28dac-106">El mensaje de **\_ \_ finalización DECOMPRESSEX de ICM** notifica a un controlador de descompresión de vídeo que finalice la descompresión y libere los recursos asignados para la descompresión.</span><span class="sxs-lookup"><span data-stu-id="28dac-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="28dac-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .</span><span class="sxs-lookup"><span data-stu-id="28dac-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="28dac-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28dac-108">Return Value</span></span>

<span data-ttu-id="28dac-109">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="28dac-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28dac-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28dac-110">Remarks</span></span>

<span data-ttu-id="28dac-111">El controlador libera todos los recursos asignados para el mensaje de [**\_ \_ Inicio DECOMPRESSEX de ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="28dac-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="28dac-112">[**ICM \_ DECOMPRESSEX \_ Begin**](icm-decompressex-begin.md) y **ICM \_ DECOMPRESSEX \_ End** no se anidan.</span><span class="sxs-lookup"><span data-stu-id="28dac-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="28dac-113">Si el controlador recibe **el \_ \_ Inicio de DECOMPRESSEX ICM** antes de que se detenga la descompresión con **ICM \_ DECOMPRESSEX \_ End**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="28dac-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="28dac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28dac-114">Requirements</span></span>



| <span data-ttu-id="28dac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28dac-115">Requirement</span></span> | <span data-ttu-id="28dac-116">Value</span><span class="sxs-lookup"><span data-stu-id="28dac-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28dac-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28dac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28dac-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28dac-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="28dac-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28dac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28dac-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28dac-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28dac-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28dac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28dac-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="28dac-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28dac-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="28dac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dac-124">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="28dac-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="28dac-125">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="28dac-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





