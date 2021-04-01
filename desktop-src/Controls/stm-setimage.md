---
title: Mensaje de STM_SETIMAGE (Winuser. h)
description: Una aplicación envía un \_ mensaje STM SETIMAGE para asociar una nueva imagen con un control estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996061"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="80efa-104">Mensaje de STM \_ SETIMAGE</span><span class="sxs-lookup"><span data-stu-id="80efa-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="80efa-105">Una aplicación envía un mensaje **STM \_ SETIMAGE** para asociar una nueva imagen con un control estático.</span><span class="sxs-lookup"><span data-stu-id="80efa-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="80efa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80efa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80efa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80efa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80efa-108">Especifica el tipo de imagen que se va a asociar al control estático.</span><span class="sxs-lookup"><span data-stu-id="80efa-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="80efa-109">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="80efa-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="80efa-110">Value</span><span class="sxs-lookup"><span data-stu-id="80efa-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="80efa-111">Significado</span><span class="sxs-lookup"><span data-stu-id="80efa-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="80efa-112"><dt>**mapa de bits de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="80efa-113">MyBitmap.</span><span class="sxs-lookup"><span data-stu-id="80efa-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="80efa-114"><dt>**CURSOR de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="80efa-115">Cursor.</span><span class="sxs-lookup"><span data-stu-id="80efa-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="80efa-116"><dt>**IMAGEN \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="80efa-117">Metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="80efa-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="80efa-118"><dt>**icono de imagen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="80efa-119">Icono.</span><span class="sxs-lookup"><span data-stu-id="80efa-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="80efa-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80efa-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80efa-121">Identificador de la imagen que se va a asociar al control estático.</span><span class="sxs-lookup"><span data-stu-id="80efa-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80efa-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80efa-122">Return value</span></span>

<span data-ttu-id="80efa-123">El valor devuelto es un identificador de la imagen asociada previamente al control estático, si existe; de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="80efa-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="80efa-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80efa-124">Remarks</span></span>

<span data-ttu-id="80efa-125">Para asociar una imagen a un control estático, el control debe tener el estilo adecuado.</span><span class="sxs-lookup"><span data-stu-id="80efa-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="80efa-126">En la tabla siguiente se muestra el estilo necesario para cada tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="80efa-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="80efa-127">Tipo de imagen</span><span class="sxs-lookup"><span data-stu-id="80efa-127">Image type</span></span>         | <span data-ttu-id="80efa-128">Estilo de control estático</span><span class="sxs-lookup"><span data-stu-id="80efa-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="80efa-129">mapa de bits de imagen \_</span><span class="sxs-lookup"><span data-stu-id="80efa-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="80efa-130">\_mapa de bits SS</span><span class="sxs-lookup"><span data-stu-id="80efa-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="80efa-131">CURSOR de imagen \_</span><span class="sxs-lookup"><span data-stu-id="80efa-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="80efa-132">icono de SS \_</span><span class="sxs-lookup"><span data-stu-id="80efa-132">SS\_ICON</span></span>             |
| <span data-ttu-id="80efa-133">IMAGEN \_ ENHMETAFILE</span><span class="sxs-lookup"><span data-stu-id="80efa-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="80efa-134">SS \_ ENHMETAFILE</span><span class="sxs-lookup"><span data-stu-id="80efa-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="80efa-135">icono de imagen \_</span><span class="sxs-lookup"><span data-stu-id="80efa-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="80efa-136">icono de SS \_</span><span class="sxs-lookup"><span data-stu-id="80efa-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="80efa-137">En la versión 6 de los controles de Microsoft Win32, un mapa de bits que se pasa a un control estático mediante el mensaje **STM \_ SetImage** era el mismo mapa de bits devuelto por un mensaje **STM \_ SetImage** subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="80efa-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="80efa-138">El cliente es responsable de eliminar cualquier mapa de bits enviado a un control estático.</span><span class="sxs-lookup"><span data-stu-id="80efa-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="80efa-139">Con Windows XP, si el mapa de bits pasado en el mensaje **STM \_ SETIMAGE** contiene píxeles con alfa distinto de cero, el control estático toma una copia del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="80efa-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="80efa-140">Este mapa de bits copiado lo devuelve el siguiente mensaje de **STM \_ SETIMAGE** .</span><span class="sxs-lookup"><span data-stu-id="80efa-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="80efa-141">El código de cliente puede realizar un seguimiento independiente de los mapas de bits que se pasan al control estático, pero si no comprueba y libera los mapas de bits devueltos de los mensajes de **STM \_ SETIMAGE** , se pierden los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="80efa-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80efa-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80efa-142">Requirements</span></span>



| <span data-ttu-id="80efa-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="80efa-143">Requirement</span></span> | <span data-ttu-id="80efa-144">Value</span><span class="sxs-lookup"><span data-stu-id="80efa-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80efa-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80efa-145">Minimum supported client</span></span><br/> | <span data-ttu-id="80efa-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80efa-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="80efa-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80efa-147">Minimum supported server</span></span><br/> | <span data-ttu-id="80efa-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="80efa-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="80efa-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80efa-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="80efa-150"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80efa-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="80efa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80efa-152">**STM \_ GetImage**</span><span class="sxs-lookup"><span data-stu-id="80efa-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





