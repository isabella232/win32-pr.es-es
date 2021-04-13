---
title: Mensaje de TB_LOADIMAGES (commctrl. h)
description: Carga las imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491981"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="82311-104">\_Mensaje LOADIMAGES TB</span><span class="sxs-lookup"><span data-stu-id="82311-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="82311-105">Carga las imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="82311-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="82311-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82311-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82311-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82311-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82311-108">Identificador de una lista de imágenes de botón definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="82311-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="82311-109">Este parámetro se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="82311-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="82311-110">Value</span><span class="sxs-lookup"><span data-stu-id="82311-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="82311-111">Significado</span><span class="sxs-lookup"><span data-stu-id="82311-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="82311-112"><dt>**\_ \_ color grande de hist de IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="82311-113">Mapas de bits del explorador de Windows de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="82311-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="82311-114"><dt>**\_ \_ color pequeño de hist de IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="82311-115">Mapas de bits del explorador de Windows en tamaño pequeño.</span><span class="sxs-lookup"><span data-stu-id="82311-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="82311-116"><dt>**\_ \_ color alto de IDB STD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="82311-117">Mapas de bits estándar de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="82311-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="82311-118"><dt>**\_ \_ color pequeño de IDB STD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="82311-119">Mapas de bits estándar en tamaño pequeño.</span><span class="sxs-lookup"><span data-stu-id="82311-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="82311-120"><dt>**\_ \_ color grande de la vista IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="82311-121">Vea los mapas de bits de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="82311-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="82311-122"><dt>**\_ \_ color pequeño de la vista IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="82311-123">Vea los mapas de bits en tamaño pequeño.</span><span class="sxs-lookup"><span data-stu-id="82311-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="82311-124"><dt>**HIST de IDB \_ \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="82311-125">Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado normal.</span><span class="sxs-lookup"><span data-stu-id="82311-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="82311-126"><dt>**HIST de IDB \_ \_ activo**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="82311-127">Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado activo.</span><span class="sxs-lookup"><span data-stu-id="82311-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="82311-128"><dt>**HIST de IDB \_ \_ deshabilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="82311-129">Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="82311-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="82311-130"><dt>**HIST de IDB \_ \_ presionado**</dt></span><span class="sxs-lookup"><span data-stu-id="82311-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="82311-131">Botones de desplazamiento y favoritos del explorador de Windows en estado presionado.</span><span class="sxs-lookup"><span data-stu-id="82311-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="82311-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82311-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82311-133">Identificador de instancia.</span><span class="sxs-lookup"><span data-stu-id="82311-133">Instance handle.</span></span> <span data-ttu-id="82311-134">Este parámetro debe establecerse en HINST \_ commctrl.</span><span class="sxs-lookup"><span data-stu-id="82311-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82311-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82311-135">Return value</span></span>

<span data-ttu-id="82311-136">Recuento de imágenes de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="82311-136">The count of images in the image list.</span></span> <span data-ttu-id="82311-137">Devuelve cero si la barra de herramientas no tiene una lista de imágenes o si la lista de imágenes existente está vacía.</span><span class="sxs-lookup"><span data-stu-id="82311-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="82311-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82311-138">Remarks</span></span>

<span data-ttu-id="82311-139">Debe usar los valores de índice de imagen adecuados al preparar las estructuras de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar el mensaje de [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="82311-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="82311-140">Para obtener una lista de valores de índice de imagen para estos mapas de bits predeterminados, vea [valores de índice de imagen de botón estándar](toolbar-standard-button-image-index-values.md)de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="82311-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82311-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82311-141">Examples</span></span>

<span data-ttu-id="82311-142">En el código de ejemplo siguiente se cargan las imágenes de color pequeño estándar del sistema.</span><span class="sxs-lookup"><span data-stu-id="82311-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="82311-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82311-143">Requirements</span></span>



| <span data-ttu-id="82311-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="82311-144">Requirement</span></span> | <span data-ttu-id="82311-145">Value</span><span class="sxs-lookup"><span data-stu-id="82311-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82311-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82311-146">Minimum supported client</span></span><br/> | <span data-ttu-id="82311-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82311-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82311-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82311-148">Minimum supported server</span></span><br/> | <span data-ttu-id="82311-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="82311-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82311-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82311-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="82311-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82311-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82311-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="82311-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82311-153">**TB \_ ADDBITMAP**</span><span class="sxs-lookup"><span data-stu-id="82311-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





