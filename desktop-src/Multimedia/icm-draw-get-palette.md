---
title: Mensaje de ICM_DRAW_GET_PALETTE (VFW. h)
description: El mensaje de la \_ paleta de obtención de Draw ICM \_ \_ solicita un controlador de representación para devolver una paleta.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- Mensaje de ICM_DRAW_GET_PALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078987"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="bb04e-104">Mensaje de la paleta de obtención de \_ Draw ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="bb04e-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="bb04e-105">El mensaje de la **\_ paleta de \_ obtención \_ de Draw ICM** solicita un controlador de representación para devolver una paleta.</span><span class="sxs-lookup"><span data-stu-id="bb04e-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="bb04e-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb04e-106">Return Value</span></span>

<span data-ttu-id="bb04e-107">El controlador debe devolver uno de los siguientes: un identificador de la paleta que se está usando, **null** si no tiene un identificador para devolver o ICERR no \_ compatible Si no admite paletas.</span><span class="sxs-lookup"><span data-stu-id="bb04e-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb04e-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb04e-108">Requirements</span></span>



| <span data-ttu-id="bb04e-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb04e-109">Requirement</span></span> | <span data-ttu-id="bb04e-110">Value</span><span class="sxs-lookup"><span data-stu-id="bb04e-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb04e-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb04e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="bb04e-112">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb04e-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bb04e-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb04e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="bb04e-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb04e-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bb04e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb04e-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb04e-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb04e-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb04e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb04e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb04e-118">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb04e-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="bb04e-119">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb04e-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





