---
title: Mensaje de STM_GETIMAGE (Winuser. h)
description: Una aplicación envía un \_ mensaje de STM GetImage para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078925"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="518da-104">Mensaje de STM \_ GetImage</span><span class="sxs-lookup"><span data-stu-id="518da-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="518da-105">Una aplicación envía un mensaje de **STM \_ GetImage** para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático.</span><span class="sxs-lookup"><span data-stu-id="518da-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="518da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="518da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="518da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="518da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="518da-108">Especifica el tipo de imagen que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="518da-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="518da-109">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="518da-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="518da-110">Value</span><span class="sxs-lookup"><span data-stu-id="518da-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="518da-111">Significado</span><span class="sxs-lookup"><span data-stu-id="518da-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="518da-112"><dt>**mapa de bits de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="518da-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="518da-113">MyBitmap.</span><span class="sxs-lookup"><span data-stu-id="518da-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="518da-114"><dt>**CURSOR de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="518da-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="518da-115">Cursor.</span><span class="sxs-lookup"><span data-stu-id="518da-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="518da-116"><dt>**IMAGEN \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="518da-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="518da-117">Metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="518da-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="518da-118"><dt>**icono de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="518da-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="518da-119">Icono.</span><span class="sxs-lookup"><span data-stu-id="518da-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="518da-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="518da-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="518da-121">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="518da-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="518da-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="518da-122">Return value</span></span>

<span data-ttu-id="518da-123">El valor devuelto es un identificador de la imagen, si existe; de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="518da-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="518da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="518da-124">Requirements</span></span>



| <span data-ttu-id="518da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="518da-125">Requirement</span></span> | <span data-ttu-id="518da-126">Value</span><span class="sxs-lookup"><span data-stu-id="518da-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="518da-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="518da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="518da-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="518da-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="518da-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="518da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="518da-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="518da-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="518da-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="518da-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="518da-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="518da-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="518da-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="518da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="518da-134">**STM \_ SETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="518da-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





