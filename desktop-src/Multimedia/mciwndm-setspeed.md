---
title: Mensaje de MCIWNDM_SETSPEED (VFW. h)
description: El \_ mensaje MCIWNDM SETSPEED establece la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- Mensaje de MCIWNDM_SETSPEED de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996697"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="23df2-105">MCIWNDM \_ SETSPEED</span><span class="sxs-lookup"><span data-stu-id="23df2-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="23df2-106">El mensaje **MCIWNDM \_ SETSPEED** establece la velocidad de reproducción de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="23df2-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="23df2-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="23df2-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="23df2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23df2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23df2-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span><span class="sxs-lookup"><span data-stu-id="23df2-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="23df2-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="23df2-110">Playback speed.</span></span> <span data-ttu-id="23df2-111">Especifique 1000 para velocidad normal, valores mayores para velocidades más rápidas y valores más pequeños para velocidades más lentas.</span><span class="sxs-lookup"><span data-stu-id="23df2-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23df2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23df2-112">Return Value</span></span>

<span data-ttu-id="23df2-113">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="23df2-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="23df2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23df2-114">Requirements</span></span>



| <span data-ttu-id="23df2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="23df2-115">Requirement</span></span> | <span data-ttu-id="23df2-116">Value</span><span class="sxs-lookup"><span data-stu-id="23df2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23df2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23df2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23df2-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23df2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="23df2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23df2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23df2-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23df2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23df2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23df2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="23df2-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="23df2-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23df2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="23df2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23df2-124">**MCIWndSetSpeed**</span><span class="sxs-lookup"><span data-stu-id="23df2-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





