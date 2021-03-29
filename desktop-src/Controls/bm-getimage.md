---
title: Mensaje de BM_GETIMAGE (Winuser. h)
description: Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359792"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="51ab8-104">\_Mensaje GetImage de BM</span><span class="sxs-lookup"><span data-stu-id="51ab8-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="51ab8-105">Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.</span><span class="sxs-lookup"><span data-stu-id="51ab8-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="51ab8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51ab8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ab8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51ab8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51ab8-108">Tipo de imagen que se va a asociar al botón.</span><span class="sxs-lookup"><span data-stu-id="51ab8-108">The type of image to associate with the button.</span></span> <span data-ttu-id="51ab8-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="51ab8-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="51ab8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="51ab8-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="51ab8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="51ab8-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="51ab8-112"><dt>**mapa de bits de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51ab8-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="51ab8-113">Un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="51ab8-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="51ab8-114"><dt>**icono de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51ab8-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="51ab8-115">Un icono.</span><span class="sxs-lookup"><span data-stu-id="51ab8-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="51ab8-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51ab8-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51ab8-117">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="51ab8-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ab8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51ab8-118">Return value</span></span>

<span data-ttu-id="51ab8-119">El valor devuelto es un identificador de la imagen, si existe; de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="51ab8-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ab8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ab8-120">Requirements</span></span>



| <span data-ttu-id="51ab8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ab8-121">Requirement</span></span> | <span data-ttu-id="51ab8-122">Value</span><span class="sxs-lookup"><span data-stu-id="51ab8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ab8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ab8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="51ab8-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="51ab8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51ab8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ab8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="51ab8-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51ab8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51ab8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51ab8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ab8-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51ab8-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ab8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="51ab8-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="51ab8-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="51ab8-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51ab8-131">**BM \_ SETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="51ab8-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="51ab8-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="51ab8-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51ab8-133">Botones</span><span class="sxs-lookup"><span data-stu-id="51ab8-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





