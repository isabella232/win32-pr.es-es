---
title: Mensaje de MCIWNDM_SETPALETTE (VFW. h)
description: El \_ mensaje SETPALETTE de MCIWNDM envía un identificador de paleta al dispositivo MCI asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- Mensaje de MCIWNDM_SETPALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491722"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="01b5a-105">MCIWNDM \_ SETPALETTE</span><span class="sxs-lookup"><span data-stu-id="01b5a-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="01b5a-106">El **mensaje \_ SETPALETTE de MCIWNDM** envía un identificador de paleta al dispositivo MCI asociado a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="01b5a-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="01b5a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="01b5a-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="01b5a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01b5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b5a-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="01b5a-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="01b5a-110">Identificador de la paleta.</span><span class="sxs-lookup"><span data-stu-id="01b5a-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b5a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01b5a-111">Return Value</span></span>

<span data-ttu-id="01b5a-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01b5a-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b5a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b5a-113">Requirements</span></span>



| <span data-ttu-id="01b5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b5a-114">Requirement</span></span> | <span data-ttu-id="01b5a-115">Value</span><span class="sxs-lookup"><span data-stu-id="01b5a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01b5a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01b5a-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="01b5a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01b5a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01b5a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01b5a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01b5a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01b5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b5a-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b5a-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b5a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="01b5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b5a-123">**MCIWndSetPalette**</span><span class="sxs-lookup"><span data-stu-id="01b5a-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





