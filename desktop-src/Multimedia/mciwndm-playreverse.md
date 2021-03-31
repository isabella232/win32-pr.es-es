---
title: Mensaje de MCIWNDM_PLAYREVERSE (VFW. h)
description: El \_ mensaje MCIWNDM PLAYREVERSE reproduce el contenido actual en dirección inversa, comenzando en la posición actual y terminando al principio del contenido o hasta que otro comando detenga la reproducción.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Mensaje de MCIWNDM_PLAYREVERSE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149873"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="550c0-104">MCIWNDM \_ PLAYREVERSE</span><span class="sxs-lookup"><span data-stu-id="550c0-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="550c0-105">El mensaje **MCIWNDM \_ PLAYREVERSE** reproduce el contenido actual en dirección inversa, comenzando en la posición actual y terminando al principio del contenido o hasta que otro comando detenga la reproducción.</span><span class="sxs-lookup"><span data-stu-id="550c0-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="550c0-106">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="550c0-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="550c0-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="550c0-107">Return Value</span></span>

<span data-ttu-id="550c0-108">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="550c0-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="550c0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="550c0-109">Requirements</span></span>



| <span data-ttu-id="550c0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="550c0-110">Requirement</span></span> | <span data-ttu-id="550c0-111">Value</span><span class="sxs-lookup"><span data-stu-id="550c0-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="550c0-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="550c0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="550c0-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="550c0-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="550c0-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="550c0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="550c0-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="550c0-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="550c0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="550c0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="550c0-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="550c0-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550c0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="550c0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550c0-119">**MCIWndPlayReverse**</span><span class="sxs-lookup"><span data-stu-id="550c0-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





