---
title: Constantes de TS_SHIFT_ (Textstor. h)
description: La \_ \_ interfaz IAnchor utiliza las constantes Shift de TS para manipular el texto oculto y el recuento de caracteres.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422331"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="4ae7c-103">\_Constantes de desplazamiento de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="4ae7c-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="4ae7c-104">La \_ \_ \* interfaz **IAnchor** utiliza las constantes de desplazamiento de TS para manipular el texto oculto y el recuento de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="4ae7c-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="4ae7c-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="4ae7c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ae7c-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="4ae7c-107"><dt>**TS \_ Número de TURNOs \_ \_ oculto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="4ae7c-108">Especifica que el delimitador se desplazará al límite de la región siguiente, incluido el límite de una región de texto oculto.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="4ae7c-109">Si no se establece, el delimitador se desplazará más allá de cualquier texto oculto adyacente hasta que se encuentre una región de texto visible.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="4ae7c-110"><dt>**TS \_ DESPLAZAMIENTO \_ detenido \_ oculto**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="4ae7c-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="4ae7c-112"><dt>**TS \_ Mayús \_ Halt \_ visible**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="4ae7c-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="4ae7c-114"><dt>**TS \_ \_ \_ Solo recuento de desplazamiento**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="4ae7c-115">No se desplaza el delimitador.</span><span class="sxs-lookup"><span data-stu-id="4ae7c-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="4ae7c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae7c-116">Requirements</span></span>



| <span data-ttu-id="4ae7c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae7c-117">Requirement</span></span> | <span data-ttu-id="4ae7c-118">Value</span><span class="sxs-lookup"><span data-stu-id="4ae7c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae7c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae7c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ae7c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4ae7c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae7c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ae7c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ae7c-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4ae7c-123">Redistributable</span></span><br/>          | <span data-ttu-id="4ae7c-124">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ae7c-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="4ae7c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae7c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ae7c-126"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ae7c-127">IDL</span><span class="sxs-lookup"><span data-stu-id="4ae7c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ae7c-128"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ae7c-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae7c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ae7c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae7c-130">IAnchor::ShiftRegion</span><span class="sxs-lookup"><span data-stu-id="4ae7c-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





