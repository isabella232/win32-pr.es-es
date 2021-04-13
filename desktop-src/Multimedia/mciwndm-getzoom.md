---
title: Mensaje de MCIWNDM_GETZOOM (VFW. h)
description: El \_ mensaje MCIWNDM GETZOOM recupera el valor de zoom actual usado por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- Mensaje de MCIWNDM_GETZOOM de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490120"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="6bff9-105">MCIWNDM \_ GETZOOM</span><span class="sxs-lookup"><span data-stu-id="6bff9-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="6bff9-106">El mensaje **MCIWNDM \_ GETZOOM** recupera el valor de zoom actual usado por un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6bff9-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="6bff9-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="6bff9-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6bff9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bff9-108">Return Value</span></span>

<span data-ttu-id="6bff9-109">Devuelve los valores más recientes utilizados con [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md).</span><span class="sxs-lookup"><span data-stu-id="6bff9-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6bff9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bff9-110">Remarks</span></span>

<span data-ttu-id="6bff9-111">Un valor devuelto de 100 indica que la imagen no se ha ampliado.</span><span class="sxs-lookup"><span data-stu-id="6bff9-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="6bff9-112">Un valor de 200 indica que la imagen se amplía hasta el doble del tamaño original.</span><span class="sxs-lookup"><span data-stu-id="6bff9-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="6bff9-113">Un valor de 50 indica que la imagen se reduce a la mitad de su tamaño original.</span><span class="sxs-lookup"><span data-stu-id="6bff9-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bff9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bff9-114">Requirements</span></span>



| <span data-ttu-id="6bff9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bff9-115">Requirement</span></span> | <span data-ttu-id="6bff9-116">Value</span><span class="sxs-lookup"><span data-stu-id="6bff9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6bff9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bff9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bff9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6bff9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6bff9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bff9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bff9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6bff9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6bff9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bff9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bff9-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bff9-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bff9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bff9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bff9-124">**MCIWndGetZoom**</span><span class="sxs-lookup"><span data-stu-id="6bff9-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="6bff9-125">**MCIWNDM \_ SETZOOM**</span><span class="sxs-lookup"><span data-stu-id="6bff9-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





