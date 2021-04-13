---
title: Mensaje de MCIWNDM_EJECT (VFW. h)
description: El \_ mensaje MCIWNDM EJECT envía un comando a un dispositivo MCI para expulsar el contenido multimedia. Puede enviar este mensaje explícitamente o mediante la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- Mensaje de MCIWNDM_EJECT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422045"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="ad085-105">MCIWNDM \_ expulsar mensaje</span><span class="sxs-lookup"><span data-stu-id="ad085-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="ad085-106">El mensaje **MCIWNDM \_ EJECT** envía un comando a un dispositivo MCI para expulsar el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad085-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="ad085-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .</span><span class="sxs-lookup"><span data-stu-id="ad085-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ad085-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad085-108">Return Value</span></span>

<span data-ttu-id="ad085-109">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ad085-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad085-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad085-110">Requirements</span></span>



| <span data-ttu-id="ad085-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad085-111">Requirement</span></span> | <span data-ttu-id="ad085-112">Value</span><span class="sxs-lookup"><span data-stu-id="ad085-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ad085-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad085-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ad085-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ad085-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ad085-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad085-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ad085-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad085-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ad085-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad085-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad085-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad085-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad085-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad085-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad085-120">**MCIWndEject**</span><span class="sxs-lookup"><span data-stu-id="ad085-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





