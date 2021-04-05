---
title: Mensaje de MCIWNDM_GET_DEST (VFW. h)
description: El \_ mensaje MCIWNDM Get \_ dest recupera las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- Mensaje de MCIWNDM_GET_DEST de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078839"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="9b37b-105">MCIWNDM \_ obtener \_ mensaje dest</span><span class="sxs-lookup"><span data-stu-id="9b37b-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="9b37b-106">El mensaje **MCIWNDM \_ Get \_ dest** recupera las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un archivo AVI durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9b37b-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="9b37b-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .</span><span class="sxs-lookup"><span data-stu-id="9b37b-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="9b37b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b37b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b37b-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="9b37b-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="9b37b-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para devolver las coordenadas del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="9b37b-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b37b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b37b-111">Return Value</span></span>

<span data-ttu-id="9b37b-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9b37b-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b37b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b37b-113">Requirements</span></span>



| <span data-ttu-id="9b37b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b37b-114">Requirement</span></span> | <span data-ttu-id="9b37b-115">Value</span><span class="sxs-lookup"><span data-stu-id="9b37b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9b37b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b37b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9b37b-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9b37b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9b37b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b37b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9b37b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b37b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9b37b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b37b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b37b-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b37b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b37b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b37b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b37b-123">**MCIWndGetDest**</span><span class="sxs-lookup"><span data-stu-id="9b37b-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

