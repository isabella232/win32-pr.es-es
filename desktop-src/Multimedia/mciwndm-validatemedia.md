---
title: Mensaje de MCIWNDM_VALIDATEMEDIA (VFW. h)
description: El \_ mensaje MCIWNDM VALIDATEMEDIA actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y el TrackBar según el formato de hora actual.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- Mensaje de MCIWNDM_VALIDATEMEDIA de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533796"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="e0a9a-104">MCIWNDM \_ VALIDATEMEDIA</span><span class="sxs-lookup"><span data-stu-id="e0a9a-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="e0a9a-105">El mensaje **MCIWNDM \_ VALIDATEMEDIA** actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y el TrackBar según el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="e0a9a-106">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .</span><span class="sxs-lookup"><span data-stu-id="e0a9a-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e0a9a-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0a9a-107">Return Value</span></span>

<span data-ttu-id="e0a9a-108">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a9a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0a9a-109">Remarks</span></span>

<span data-ttu-id="e0a9a-110">Normalmente, no es necesario usar esta macro; sin embargo, si la aplicación cambia el formato de hora de un dispositivo sin usar MCIWnd; las ubicaciones inicial y final del contenido, así como la barra de inicio, siguen usando el formato antiguo.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="e0a9a-111">Puede usar esta macro para actualizar estos valores.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a9a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a9a-112">Requirements</span></span>



| <span data-ttu-id="e0a9a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a9a-113">Requirement</span></span> | <span data-ttu-id="e0a9a-114">Value</span><span class="sxs-lookup"><span data-stu-id="e0a9a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0a9a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a9a-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e0a9a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e0a9a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a9a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0a9a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e0a9a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0a9a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0a9a-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0a9a-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a9a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a9a-122">**MCIWndValidateMedia**</span><span class="sxs-lookup"><span data-stu-id="e0a9a-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





