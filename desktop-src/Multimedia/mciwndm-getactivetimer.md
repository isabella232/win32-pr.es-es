---
title: Mensaje de MCIWNDM_GETACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM GETACTIVETIMER recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- Mensaje de MCIWNDM_GETACTIVETIMER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151236"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="ab738-105">MCIWNDM \_ GETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="ab738-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="ab738-106">El mensaje **MCIWNDM \_ GETACTIVETIMER** recupera el período de actualización que se usa cuando la ventana de MCIWnd es la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="ab738-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="ab738-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="ab738-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="ab738-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab738-108">Return Value</span></span>

<span data-ttu-id="ab738-109">Devuelve el período de actualización en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ab738-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="ab738-110">El valor predeterminado es 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ab738-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab738-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab738-111">Requirements</span></span>



| <span data-ttu-id="ab738-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab738-112">Requirement</span></span> | <span data-ttu-id="ab738-113">Value</span><span class="sxs-lookup"><span data-stu-id="ab738-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab738-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab738-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ab738-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab738-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab738-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab738-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ab738-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab738-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab738-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab738-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab738-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab738-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab738-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab738-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab738-121">**MCIWndGetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="ab738-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





