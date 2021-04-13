---
title: Mensaje de MCIWNDM_GETSTART (VFW. h)
description: El \_ mensaje GETSTART de MCIWNDM recupera la ubicación del inicio del contenido de un dispositivo o archivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- Mensaje de MCIWNDM_GETSTART de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489418"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="e1745-105">MCIWNDM \_ GETSTART</span><span class="sxs-lookup"><span data-stu-id="e1745-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="e1745-106">El **mensaje \_ GETSTART de MCIWNDM** recupera la ubicación del inicio del contenido de un dispositivo o archivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e1745-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="e1745-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .</span><span class="sxs-lookup"><span data-stu-id="e1745-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e1745-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1745-108">Return Value</span></span>

<span data-ttu-id="e1745-109">Devuelve la ubicación en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="e1745-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1745-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1745-110">Remarks</span></span>

<span data-ttu-id="e1745-111">Normalmente, el valor devuelto es cero; pero algunos dispositivos usan una ubicación de inicio distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e1745-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="e1745-112">Al buscar en esta ubicación, el dispositivo se establece en el inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="e1745-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1745-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1745-113">Requirements</span></span>



| <span data-ttu-id="e1745-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1745-114">Requirement</span></span> | <span data-ttu-id="e1745-115">Value</span><span class="sxs-lookup"><span data-stu-id="e1745-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1745-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1745-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e1745-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1745-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1745-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1745-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e1745-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1745-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1745-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1745-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1745-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1745-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1745-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1745-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1745-123">**MCIWndGetStart**</span><span class="sxs-lookup"><span data-stu-id="e1745-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





