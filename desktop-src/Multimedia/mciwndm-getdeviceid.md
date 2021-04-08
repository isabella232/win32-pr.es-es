---
title: Mensaje de MCIWNDM_GETDEVICEID (VFW. h)
description: El \_ mensaje GETDEVICEID de MCIWNDM recupera el identificador del dispositivo MCI abierto actualmente para usarlo con la función mciSendCommand. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- Mensaje de MCIWNDM_GETDEVICEID de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078981"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="f3d07-105">MCIWNDM \_ GETDEVICEID</span><span class="sxs-lookup"><span data-stu-id="f3d07-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="f3d07-106">El **mensaje \_ GETDEVICEID de MCIWNDM** recupera el identificador del dispositivo MCI abierto actualmente para usarlo con la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f3d07-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="f3d07-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="f3d07-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f3d07-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3d07-108">Return Value</span></span>

<span data-ttu-id="f3d07-109">Devuelve el identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3d07-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d07-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3d07-110">Requirements</span></span>



| <span data-ttu-id="f3d07-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d07-111">Requirement</span></span> | <span data-ttu-id="f3d07-112">Value</span><span class="sxs-lookup"><span data-stu-id="f3d07-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3d07-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3d07-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d07-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f3d07-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3d07-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3d07-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d07-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3d07-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3d07-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3d07-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3d07-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3d07-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d07-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3d07-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3d07-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3d07-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3d07-121">**MCIWndGetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f3d07-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

