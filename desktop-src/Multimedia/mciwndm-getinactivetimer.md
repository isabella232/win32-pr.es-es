---
title: Mensaje de MCIWNDM_GETINACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM GETINACTIVETIMER recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- Mensaje de MCIWNDM_GETINACTIVETIMER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676591"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="28c0f-105">MCIWNDM \_ GETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="28c0f-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="28c0f-106">El mensaje **MCIWNDM \_ GETINACTIVETIMER** recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana inactiva.</span><span class="sxs-lookup"><span data-stu-id="28c0f-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="28c0f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="28c0f-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="28c0f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28c0f-108">Return Value</span></span>

<span data-ttu-id="28c0f-109">Devuelve el período de actualización, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="28c0f-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="28c0f-110">El valor predeterminado es 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="28c0f-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c0f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c0f-111">Requirements</span></span>



| <span data-ttu-id="28c0f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c0f-112">Requirement</span></span> | <span data-ttu-id="28c0f-113">Value</span><span class="sxs-lookup"><span data-stu-id="28c0f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28c0f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c0f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="28c0f-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28c0f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="28c0f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c0f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="28c0f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28c0f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28c0f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28c0f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c0f-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c0f-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c0f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="28c0f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c0f-121">**MCIWndGetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="28c0f-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





