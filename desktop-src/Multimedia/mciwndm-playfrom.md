---
title: Mensaje de MCIWNDM_PLAYFROM (VFW. h)
description: El \_ mensaje MCIWNDM PLAYFROM reproduce el contenido de un dispositivo MCI desde la ubicación especificada hasta el final del contenido o hasta que otro comando detiene la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- Mensaje de MCIWNDM_PLAYFROM de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996044"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="421f4-105">MCIWNDM \_ PLAYFROM</span><span class="sxs-lookup"><span data-stu-id="421f4-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="421f4-106">El mensaje **MCIWNDM \_ PLAYFROM** reproduce el contenido de un dispositivo MCI desde la ubicación especificada hasta el final del contenido o hasta que otro comando detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="421f4-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="421f4-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="421f4-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="421f4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="421f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="421f4-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="421f4-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="421f4-110">Ubicación inicial.</span><span class="sxs-lookup"><span data-stu-id="421f4-110">Starting location.</span></span> <span data-ttu-id="421f4-111">Las unidades de la ubicación inicial dependen del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="421f4-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="421f4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="421f4-112">Return Value</span></span>

<span data-ttu-id="421f4-113">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="421f4-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="421f4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="421f4-114">Remarks</span></span>

<span data-ttu-id="421f4-115">También puede especificar una ubicación inicial y final para la reproducción mediante la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="421f4-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="421f4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="421f4-116">Requirements</span></span>



| <span data-ttu-id="421f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="421f4-117">Requirement</span></span> | <span data-ttu-id="421f4-118">Value</span><span class="sxs-lookup"><span data-stu-id="421f4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="421f4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="421f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="421f4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="421f4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="421f4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="421f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="421f4-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="421f4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="421f4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="421f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="421f4-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="421f4-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="421f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="421f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421f4-126">**MCIWndPlayFrom**</span><span class="sxs-lookup"><span data-stu-id="421f4-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="421f4-127">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="421f4-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





