---
title: Mensaje de ICM_DRAW_END (VFW. h)
description: El \_ mensaje de \_ finalización del dibujo ICM notifica a un controlador de representación que descomprima la imagen actual en la pantalla y libere los recursos asignados para la descompresión y el dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Mensaje de ICM_DRAW_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802623"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="2498b-105">\_Mensaje final de Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="2498b-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="2498b-106">El mensaje de **\_ \_ finalización del dibujo ICM** notifica a un controlador de representación que descomprima la imagen actual en la pantalla y libere los recursos asignados para la descompresión y el dibujo.</span><span class="sxs-lookup"><span data-stu-id="2498b-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="2498b-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="2498b-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2498b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2498b-108">Return Value</span></span>

<span data-ttu-id="2498b-109">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2498b-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2498b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2498b-110">Remarks</span></span>

<span data-ttu-id="2498b-111">Los mensajes de [**\_ \_ Inicio de dibujo de ICM**](icm-draw-begin.md) y **\_ \_ fin de dibujo de ICM** no se anidan.</span><span class="sxs-lookup"><span data-stu-id="2498b-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="2498b-112">Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la descompresión con el **\_ \_ extremo de Draw ICM**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="2498b-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2498b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2498b-113">Requirements</span></span>



| <span data-ttu-id="2498b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2498b-114">Requirement</span></span> | <span data-ttu-id="2498b-115">Value</span><span class="sxs-lookup"><span data-stu-id="2498b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2498b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2498b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2498b-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2498b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2498b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2498b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2498b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2498b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2498b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2498b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2498b-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2498b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2498b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2498b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2498b-123">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2498b-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2498b-124">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2498b-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





