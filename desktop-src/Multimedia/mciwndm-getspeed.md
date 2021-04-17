---
title: Mensaje de MCIWNDM_GETSPEED (VFW. h)
description: El \_ mensaje MCIWNDM GETSPEED recupera la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- Mensaje de MCIWNDM_GETSPEED de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492820"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="4cce7-105">MCIWNDM \_ GETSPEED</span><span class="sxs-lookup"><span data-stu-id="4cce7-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="4cce7-106">El mensaje **MCIWNDM \_ GETSPEED** recupera la velocidad de reproducción de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4cce7-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="4cce7-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="4cce7-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="4cce7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cce7-108">Return Value</span></span>

<span data-ttu-id="4cce7-109">Devuelve la velocidad de reproducción si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4cce7-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="4cce7-110">El valor de velocidad normal es 1000.</span><span class="sxs-lookup"><span data-stu-id="4cce7-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="4cce7-111">Los valores más grandes indican velocidades más rápidas, los valores más pequeños indican velocidades más lentas.</span><span class="sxs-lookup"><span data-stu-id="4cce7-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cce7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cce7-112">Requirements</span></span>



| <span data-ttu-id="4cce7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cce7-113">Requirement</span></span> | <span data-ttu-id="4cce7-114">Value</span><span class="sxs-lookup"><span data-stu-id="4cce7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4cce7-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cce7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4cce7-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4cce7-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4cce7-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cce7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4cce7-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4cce7-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4cce7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cce7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cce7-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cce7-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cce7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cce7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cce7-122">**MCIWndGetSpeed**</span><span class="sxs-lookup"><span data-stu-id="4cce7-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





