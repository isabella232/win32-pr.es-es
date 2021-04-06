---
title: Mensaje de MCIWNDM_GETPALETTE (VFW. h)
description: El \_ mensaje GETPALETTE de MCIWNDM recupera un identificador de la paleta usada por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- Mensaje de MCIWNDM_GETPALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078980"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="4247b-105">MCIWNDM \_ GETPALETTE</span><span class="sxs-lookup"><span data-stu-id="4247b-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="4247b-106">El **mensaje \_ GETPALETTE de MCIWNDM** recupera un identificador de la paleta usada por un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4247b-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="4247b-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="4247b-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="4247b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4247b-108">Return Value</span></span>

<span data-ttu-id="4247b-109">Devuelve el identificador de la paleta si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4247b-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4247b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4247b-110">Requirements</span></span>



| <span data-ttu-id="4247b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4247b-111">Requirement</span></span> | <span data-ttu-id="4247b-112">Value</span><span class="sxs-lookup"><span data-stu-id="4247b-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4247b-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4247b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4247b-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4247b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4247b-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4247b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4247b-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4247b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4247b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4247b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4247b-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4247b-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4247b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4247b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4247b-120">**MCIWndGetPalette**</span><span class="sxs-lookup"><span data-stu-id="4247b-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





