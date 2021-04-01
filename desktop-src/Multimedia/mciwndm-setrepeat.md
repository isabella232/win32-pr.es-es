---
title: Mensaje de MCIWNDM_SETREPEAT (VFW. h)
description: El \_ mensaje MCIWNDM SETREPEAT establece la marca de repetición asociada con la reproducción continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- Mensaje de MCIWNDM_SETREPEAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905414"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="2eb23-104">MCIWNDM \_ SETREPEAT</span><span class="sxs-lookup"><span data-stu-id="2eb23-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="2eb23-105">El mensaje **MCIWNDM \_ SETREPEAT** establece la marca de repetición asociada con la reproducción continua.</span><span class="sxs-lookup"><span data-stu-id="2eb23-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="2eb23-106">El mensaje **MCIWNDM \_ SETREPEAT** funciona junto con el comando [MCI \_ Play](mci-play.md) para proporcionar un bucle de reproducción continuo.</span><span class="sxs-lookup"><span data-stu-id="2eb23-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="2eb23-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="2eb23-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="2eb23-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eb23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb23-109"><span id="f"></span><span id="F"></span>*formato*</span><span class="sxs-lookup"><span data-stu-id="2eb23-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="2eb23-110">Nuevo estado de la marca de repetición.</span><span class="sxs-lookup"><span data-stu-id="2eb23-110">New state of the repeat flag.</span></span> <span data-ttu-id="2eb23-111">Especifique **true** para activar la reproducción continua.</span><span class="sxs-lookup"><span data-stu-id="2eb23-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb23-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eb23-112">Return Value</span></span>

<span data-ttu-id="2eb23-113">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2eb23-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb23-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eb23-114">Remarks</span></span>

<span data-ttu-id="2eb23-115">Actualmente, MCIAVI es el único dispositivo que admite la reproducción continua.</span><span class="sxs-lookup"><span data-stu-id="2eb23-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb23-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb23-116">Requirements</span></span>



| <span data-ttu-id="2eb23-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb23-117">Requirement</span></span> | <span data-ttu-id="2eb23-118">Value</span><span class="sxs-lookup"><span data-stu-id="2eb23-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2eb23-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb23-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb23-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2eb23-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2eb23-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb23-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb23-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2eb23-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2eb23-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2eb23-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb23-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb23-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb23-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eb23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb23-126">reproducción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2eb23-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="2eb23-127">**MCIWndSetRepeat**</span><span class="sxs-lookup"><span data-stu-id="2eb23-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





