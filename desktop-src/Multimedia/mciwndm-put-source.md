---
title: Mensaje de MCIWNDM_PUT_SOURCE (VFW. h)
description: El \_ \_ mensaje de origen put de MCIWNDM vuelve a definir las coordenadas del rectángulo de origen que se usa para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- Mensaje de MCIWNDM_PUT_SOURCE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801010"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="e2f1d-105">MCIWNDM \_ colocar \_ mensaje de origen</span><span class="sxs-lookup"><span data-stu-id="e2f1d-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="e2f1d-106">El mensaje de **\_ \_ origen put de MCIWNDM** vuelve a definir las coordenadas del rectángulo de origen que se usa para recortar las imágenes de un archivo AVI durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e2f1d-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="e2f1d-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .</span><span class="sxs-lookup"><span data-stu-id="e2f1d-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="e2f1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2f1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f1d-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="e2f1d-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="e2f1d-110">Puntero a una estructura [Rect](/previous-versions//ms536136(v=vs.85)) que contiene las coordenadas del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="e2f1d-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f1d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f1d-111">Return Value</span></span>

<span data-ttu-id="e2f1d-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e2f1d-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f1d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f1d-113">Requirements</span></span>



| <span data-ttu-id="e2f1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f1d-114">Requirement</span></span> | <span data-ttu-id="e2f1d-115">Value</span><span class="sxs-lookup"><span data-stu-id="e2f1d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2f1d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f1d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e2f1d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e2f1d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f1d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2f1d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2f1d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2f1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f1d-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f1d-121"><dt>Vfw.h</dt></span></span> </dl> |



 

