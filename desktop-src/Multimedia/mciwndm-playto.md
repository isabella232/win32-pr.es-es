---
title: Mensaje de MCIWNDM_PLAYTO (VFW. h)
description: El \_ mensaje MCIWNDM playto reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro comando detiene la reproducción.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Mensaje de MCIWNDM_PLAYTO de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150869"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="066be-104">Mensaje de MCIWNDM \_ playto</span><span class="sxs-lookup"><span data-stu-id="066be-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="066be-105">El mensaje **MCIWNDM \_ playto** reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro comando detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="066be-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="066be-106">Si la ubicación de finalización especificada está más allá del final del contenido, la reproducción se detiene al final del contenido.</span><span class="sxs-lookup"><span data-stu-id="066be-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="066be-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="066be-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="066be-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="066be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066be-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Acreedor*</span><span class="sxs-lookup"><span data-stu-id="066be-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="066be-110">Ubicación final.</span><span class="sxs-lookup"><span data-stu-id="066be-110">Ending location.</span></span> <span data-ttu-id="066be-111">Las unidades de la ubicación de finalización dependen del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="066be-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="066be-112">Return Value</span></span>

<span data-ttu-id="066be-113">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="066be-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="066be-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="066be-114">Remarks</span></span>

<span data-ttu-id="066be-115">Esta macro se define mediante las macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) y [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , que a su vez usan el comando [MCI \_ Seek](mci-seek.md) y el mensaje **MCIWNDM \_ playto** .</span><span class="sxs-lookup"><span data-stu-id="066be-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="066be-116">También puede especificar una ubicación inicial y final para la reproducción mediante la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="066be-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="066be-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="066be-117">Requirements</span></span>



| <span data-ttu-id="066be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="066be-118">Requirement</span></span> | <span data-ttu-id="066be-119">Value</span><span class="sxs-lookup"><span data-stu-id="066be-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="066be-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="066be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="066be-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="066be-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="066be-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="066be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="066be-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="066be-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="066be-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="066be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="066be-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="066be-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066be-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="066be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066be-127">búsqueda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="066be-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="066be-128">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="066be-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="066be-129">**MCIWndPlayTo**</span><span class="sxs-lookup"><span data-stu-id="066be-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="066be-130">**MCIWndSeek**</span><span class="sxs-lookup"><span data-stu-id="066be-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





