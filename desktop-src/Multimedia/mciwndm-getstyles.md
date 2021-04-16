---
title: Mensaje de MCIWNDM_GETSTYLES (VFW. h)
description: El \_ mensaje GETSTYLES de MCIWNDM recupera las marcas que especifican los estilos de ventana de MCIWnd actuales usados por una ventana. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- Mensaje de MCIWNDM_GETSTYLES de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676949"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="ab60a-105">MCIWNDM \_ GETSTYLES</span><span class="sxs-lookup"><span data-stu-id="ab60a-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="ab60a-106">El **mensaje \_ GETSTYLES de MCIWNDM** recupera las marcas que especifican los estilos de ventana de MCIWnd actuales usados por una ventana.</span><span class="sxs-lookup"><span data-stu-id="ab60a-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="ab60a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="ab60a-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ab60a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab60a-108">Return Value</span></span>

<span data-ttu-id="ab60a-109">Devuelve un valor que representa los estilos actuales de la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ab60a-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="ab60a-110">El valor devuelto es el operador OR bit a bit de los estilos de ventana MCIWnd (marcas MCIWNDF).</span><span class="sxs-lookup"><span data-stu-id="ab60a-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab60a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab60a-111">Requirements</span></span>



| <span data-ttu-id="ab60a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab60a-112">Requirement</span></span> | <span data-ttu-id="ab60a-113">Value</span><span class="sxs-lookup"><span data-stu-id="ab60a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab60a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab60a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ab60a-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab60a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab60a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab60a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ab60a-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab60a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab60a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab60a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab60a-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab60a-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab60a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab60a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab60a-121">**MCIWndGetStyles**</span><span class="sxs-lookup"><span data-stu-id="ab60a-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





