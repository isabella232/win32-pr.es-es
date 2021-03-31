---
title: Mensaje de MCIWNDM_SETVOLUME (VFW. h)
description: El \_ mensaje MCIWNDM SETVOLUME establece el nivel de volumen de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- Mensaje de MCIWNDM_SETVOLUME de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801322"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="016e4-105">MCIWNDM \_ SETVOLUME</span><span class="sxs-lookup"><span data-stu-id="016e4-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="016e4-106">El mensaje **MCIWNDM \_ SETVOLUME** establece el nivel de volumen de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="016e4-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="016e4-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="016e4-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="016e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="016e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="016e4-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span><span class="sxs-lookup"><span data-stu-id="016e4-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="016e4-110">Nuevo nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="016e4-110">New volume level.</span></span> <span data-ttu-id="016e4-111">Especifique 1000 para el nivel de volumen normal.</span><span class="sxs-lookup"><span data-stu-id="016e4-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="016e4-112">Especifique un valor mayor para un volumen más alto o un valor inferior para un volumen más silencioso.</span><span class="sxs-lookup"><span data-stu-id="016e4-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="016e4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="016e4-113">Return Value</span></span>

<span data-ttu-id="016e4-114">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="016e4-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="016e4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="016e4-115">Requirements</span></span>



| <span data-ttu-id="016e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="016e4-116">Requirement</span></span> | <span data-ttu-id="016e4-117">Value</span><span class="sxs-lookup"><span data-stu-id="016e4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="016e4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="016e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="016e4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="016e4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="016e4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="016e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="016e4-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="016e4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="016e4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="016e4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="016e4-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="016e4-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016e4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="016e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016e4-125">**MCIWndSetVolume**</span><span class="sxs-lookup"><span data-stu-id="016e4-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





