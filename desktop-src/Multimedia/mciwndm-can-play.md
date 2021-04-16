---
title: Mensaje de MCIWNDM_CAN_PLAY (VFW. h)
description: El \_ mensaje MCIWNDM puede \_ reproducir determina si un dispositivo MCI puede reproducir un archivo de datos o contenido de algún otro tipo. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- Mensaje de MCIWNDM_CAN_PLAY de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676981"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="7bf15-105">MCIWNDM \_ puede \_ reproducir el mensaje</span><span class="sxs-lookup"><span data-stu-id="7bf15-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="7bf15-106">El mensaje **MCIWNDM \_ puede \_ reproducir** determina si un dispositivo MCI puede reproducir un archivo de datos o contenido de algún otro tipo.</span><span class="sxs-lookup"><span data-stu-id="7bf15-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="7bf15-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .</span><span class="sxs-lookup"><span data-stu-id="7bf15-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7bf15-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bf15-108">Return Value</span></span>

<span data-ttu-id="7bf15-109">Devuelve **true** si el dispositivo admite la reproducción de los datos o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7bf15-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf15-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bf15-110">Requirements</span></span>



| <span data-ttu-id="7bf15-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf15-111">Requirement</span></span> | <span data-ttu-id="7bf15-112">Value</span><span class="sxs-lookup"><span data-stu-id="7bf15-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7bf15-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bf15-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf15-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7bf15-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7bf15-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bf15-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf15-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bf15-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7bf15-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bf15-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf15-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf15-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf15-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bf15-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf15-120">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="7bf15-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





