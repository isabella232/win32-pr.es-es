---
title: Mensaje de MCIWNDM_GETREPEAT (VFW. h)
description: El \_ mensaje GETREPEAT de MCIWNDM determina si se ha activado la reproducción continua. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- Mensaje de MCIWNDM_GETREPEAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149978"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="5f99e-105">MCIWNDM \_ GETREPEAT</span><span class="sxs-lookup"><span data-stu-id="5f99e-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="5f99e-106">El **mensaje \_ GETREPEAT de MCIWNDM** determina si se ha activado la reproducción continua.</span><span class="sxs-lookup"><span data-stu-id="5f99e-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="5f99e-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="5f99e-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5f99e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f99e-108">Return Value</span></span>

<span data-ttu-id="5f99e-109">Devuelve **true** si se activa la reproducción continua o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5f99e-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f99e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f99e-110">Requirements</span></span>



| <span data-ttu-id="5f99e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f99e-111">Requirement</span></span> | <span data-ttu-id="5f99e-112">Value</span><span class="sxs-lookup"><span data-stu-id="5f99e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f99e-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f99e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f99e-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f99e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f99e-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f99e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f99e-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f99e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f99e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f99e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f99e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f99e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f99e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f99e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f99e-120">**MCIWndGetRepeat**</span><span class="sxs-lookup"><span data-stu-id="5f99e-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





