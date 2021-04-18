---
title: Mensaje de MCIWNDM_GETVOLUME (VFW. h)
description: El \_ mensaje MCIWNDM GETVOLUME recupera la configuración del volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- Mensaje de MCIWNDM_GETVOLUME de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422581"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="ff80a-105">MCIWNDM \_ GETVOLUME</span><span class="sxs-lookup"><span data-stu-id="ff80a-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="ff80a-106">El mensaje **MCIWNDM \_ GETVOLUME** recupera la configuración del volumen actual de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ff80a-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="ff80a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="ff80a-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ff80a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff80a-108">Return Value</span></span>

<span data-ttu-id="ff80a-109">Devuelve la configuración del volumen actual.</span><span class="sxs-lookup"><span data-stu-id="ff80a-109">Returns the current volume setting.</span></span> <span data-ttu-id="ff80a-110">El valor predeterminado es 1000.</span><span class="sxs-lookup"><span data-stu-id="ff80a-110">The default value is 1000.</span></span> <span data-ttu-id="ff80a-111">Los valores más altos indican volúmenes más altos, los valores más bajos indican volúmenes más silenciosos.</span><span class="sxs-lookup"><span data-stu-id="ff80a-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff80a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff80a-112">Requirements</span></span>



| <span data-ttu-id="ff80a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff80a-113">Requirement</span></span> | <span data-ttu-id="ff80a-114">Value</span><span class="sxs-lookup"><span data-stu-id="ff80a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ff80a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff80a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ff80a-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ff80a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ff80a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff80a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ff80a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff80a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ff80a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff80a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff80a-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff80a-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff80a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff80a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff80a-122">**MCIWndGetVolume**</span><span class="sxs-lookup"><span data-stu-id="ff80a-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





