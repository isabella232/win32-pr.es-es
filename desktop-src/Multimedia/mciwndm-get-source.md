---
title: Mensaje de MCIWNDM_GET_SOURCE (VFW. h)
description: El \_ \_ mensaje de origen de MCIWNDM Get recupera las coordenadas del rectángulo de origen utilizado para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- Mensaje de MCIWNDM_GET_SOURCE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422496"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="beadc-105">MCIWNDM \_ obtener \_ mensaje de origen</span><span class="sxs-lookup"><span data-stu-id="beadc-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="beadc-106">El mensaje de **\_ \_ origen de MCIWNDM Get** recupera las coordenadas del rectángulo de origen utilizado para recortar las imágenes de un archivo AVI durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="beadc-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="beadc-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="beadc-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="beadc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beadc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beadc-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="beadc-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="beadc-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para que contenga las coordenadas del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="beadc-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beadc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beadc-111">Return Value</span></span>

<span data-ttu-id="beadc-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="beadc-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="beadc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beadc-113">Requirements</span></span>



| <span data-ttu-id="beadc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="beadc-114">Requirement</span></span> | <span data-ttu-id="beadc-115">Value</span><span class="sxs-lookup"><span data-stu-id="beadc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="beadc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beadc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="beadc-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="beadc-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="beadc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beadc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="beadc-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="beadc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="beadc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beadc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="beadc-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="beadc-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beadc-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="beadc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beadc-123">**MCIWndGetSource**</span><span class="sxs-lookup"><span data-stu-id="beadc-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

