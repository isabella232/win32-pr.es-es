---
title: Mensaje de MCIWNDM_CAN_RECORD (VFW. h)
description: El MCIWNDM \_ puede \_ grabar el mensaje determina si un dispositivo MCI admite la grabación. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- Mensaje de MCIWNDM_CAN_RECORD de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492611"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="88495-105">MCIWNDM \_ puede \_ registrar el mensaje</span><span class="sxs-lookup"><span data-stu-id="88495-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="88495-106">El **MCIWNDM \_ puede \_ grabar** el mensaje determina si un dispositivo MCI admite la grabación.</span><span class="sxs-lookup"><span data-stu-id="88495-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="88495-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .</span><span class="sxs-lookup"><span data-stu-id="88495-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="88495-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88495-108">Return Value</span></span>

<span data-ttu-id="88495-109">Devuelve **true** si el dispositivo admite la grabación o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="88495-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="88495-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88495-110">Requirements</span></span>



| <span data-ttu-id="88495-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="88495-111">Requirement</span></span> | <span data-ttu-id="88495-112">Value</span><span class="sxs-lookup"><span data-stu-id="88495-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88495-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88495-113">Minimum supported client</span></span><br/> | <span data-ttu-id="88495-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88495-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="88495-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88495-115">Minimum supported server</span></span><br/> | <span data-ttu-id="88495-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88495-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88495-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88495-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="88495-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="88495-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88495-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="88495-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88495-120">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="88495-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





