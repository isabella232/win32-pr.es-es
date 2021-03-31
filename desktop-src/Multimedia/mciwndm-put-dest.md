---
title: Mensaje de MCIWNDM_PUT_DEST (VFW. h)
description: El \_ \_ mensaje dest de MCIWNDM Put vuelve a definir las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- Mensaje de MCIWNDM_PUT_DEST de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803362"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="6ec4c-105">MCIWNDM \_ poner \_ mensaje dest</span><span class="sxs-lookup"><span data-stu-id="6ec4c-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="6ec4c-106">El **mensaje \_ \_ dest de MCIWNDM Put** vuelve a definir las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un archivo AVI durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6ec4c-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="6ec4c-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="6ec4c-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="6ec4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ec4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec4c-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="6ec4c-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="6ec4c-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6ec4c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec4c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ec4c-111">Return Value</span></span>

<span data-ttu-id="6ec4c-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6ec4c-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec4c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec4c-113">Requirements</span></span>



| <span data-ttu-id="6ec4c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec4c-114">Requirement</span></span> | <span data-ttu-id="6ec4c-115">Value</span><span class="sxs-lookup"><span data-stu-id="6ec4c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ec4c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec4c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ec4c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6ec4c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec4c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ec4c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6ec4c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec4c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec4c-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4c-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec4c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec4c-123">**MCIWndPutDest**</span><span class="sxs-lookup"><span data-stu-id="6ec4c-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

