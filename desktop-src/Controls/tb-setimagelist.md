---
title: Mensaje de TB_SETIMAGELIST (commctrl. h)
description: Establece la lista de imágenes que utiliza la barra de herramientas para mostrar los botones que se encuentran en su estado predeterminado.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- TB_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658285"
---
# <a name="tb_setimagelist-message"></a><span data-ttu-id="b0068-104">\_Mensaje SETIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="b0068-104">TB\_SETIMAGELIST message</span></span>

<span data-ttu-id="b0068-105">Establece la lista de imágenes que utiliza la barra de herramientas para mostrar los botones que se encuentran en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b0068-105">Sets the image list that the toolbar uses to display buttons that are in their default state.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0068-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0068-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0068-107">*wParam*</span></span> 
</dt> <dd>

[<span data-ttu-id="b0068-108">Versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="b0068-108">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="b0068-109">Índice de la lista.</span><span class="sxs-lookup"><span data-stu-id="b0068-109">The index of the list.</span></span> <span data-ttu-id="b0068-110">Si solo usa una lista de imágenes, o una versión anterior de los controles comunes, establezca *wParam* en cero.</span><span class="sxs-lookup"><span data-stu-id="b0068-110">If you use only one image list, or an earlier version of the common controls, set *wParam* to zero.</span></span> <span data-ttu-id="b0068-111">Vea la sección Comentarios para obtener más información sobre el uso de varias listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0068-111">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="b0068-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0068-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0068-113">Identificador de la lista de imágenes que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b0068-113">Handle to the image list to set.</span></span> <span data-ttu-id="b0068-114">Si este parámetro es **null**, no se muestra ninguna imagen en los botones.</span><span class="sxs-lookup"><span data-stu-id="b0068-114">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0068-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0068-115">Return value</span></span>

<span data-ttu-id="b0068-116">Devuelve el identificador de la lista de imágenes que se usó anteriormente para mostrar los botones en su estado predeterminado, o **null** si no se ha establecido previamente ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0068-116">Returns the handle to the image list previously used to display buttons in their default state, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0068-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0068-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0068-118">La aplicación es responsable de liberar la lista de imágenes una vez destruida la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b0068-118">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="b0068-119">El mensaje de **TB \_ SETIMAGELIST** no se puede combinar con [**TB \_ ADDBITMAP**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="b0068-119">The **TB\_SETIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="b0068-120">Tampoco se puede usar con barras de herramientas creadas con [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), que llama a **TB \_ ADDBITMAP** internamente.</span><span class="sxs-lookup"><span data-stu-id="b0068-120">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="b0068-121">Al crear una barra de herramientas con **CreateToolbarEx** o usar **TB \_ ADDBITMAP** para agregar imágenes, la barra de herramientas administra la lista de imágenes internamente.</span><span class="sxs-lookup"><span data-stu-id="b0068-121">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="b0068-122">El intento de modificarlo con **TB \_ SETIMAGELIST** tiene consecuencias imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="b0068-122">Attempting to modify it with **TB\_SETIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="b0068-123">Con la [versión 5,80](common-control-versions.md) o posterior de los controles comunes, no es necesario que las imágenes de botón provienen de la misma lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0068-123">With [version 5.80](common-control-versions.md) or later of the common controls, button images need not come from the same image list.</span></span> <span data-ttu-id="b0068-124">Para utilizar varias listas de imágenes para las imágenes de botón de la barra de herramientas:</span><span class="sxs-lookup"><span data-stu-id="b0068-124">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="b0068-125">Habilite varias listas de imágenes mediante el envío del control de barra de herramientas a un mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) con *wParam* (el número de versión) establecido en 5.</span><span class="sxs-lookup"><span data-stu-id="b0068-125">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="b0068-126">Para cada lista de imágenes que desee usar, envíe el control de barra de herramientas a un mensaje de **TB \_ SETIMAGELIST** .</span><span class="sxs-lookup"><span data-stu-id="b0068-126">For each image list you want to use, send the toolbar control a **TB\_SETIMAGELIST** message.</span></span> <span data-ttu-id="b0068-127">Establezca *wParam* en un valor *wParam* definido por la aplicación que se utilizará para identificar la lista.</span><span class="sxs-lookup"><span data-stu-id="b0068-127">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="b0068-128">Establezca *lParam* en el identificador de HIMAGELIST de la lista.</span><span class="sxs-lookup"><span data-stu-id="b0068-128">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="b0068-129">Para cada botón, establezca el miembro **iBitmap** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del botón en MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="b0068-129">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="b0068-130">El valor de *iImageID* es el identificador de la lista de imágenes adecuada que se definió en el paso dos.</span><span class="sxs-lookup"><span data-stu-id="b0068-130">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="b0068-131">El valor de *iIndex* es el índice de la imagen determinada dentro de esa lista.</span><span class="sxs-lookup"><span data-stu-id="b0068-131">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="b0068-132">Agregue los botones mediante el envío del control de barra de herramientas a un mensaje [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="b0068-132">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="b0068-133">En el fragmento de código siguiente se muestra cómo agregar cinco botones a una barra de herramientas, con imágenes de tres listas de imágenes diferentes.</span><span class="sxs-lookup"><span data-stu-id="b0068-133">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="b0068-134">La compatibilidad con varias listas de imágenes se habilita con un mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b0068-134">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="b0068-135">A continuación, se establecen y asignan los identificadores de 0-2 a las listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0068-135">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="b0068-136">A los botones se les asignan imágenes de las listas de imágenes de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b0068-136">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="b0068-137">El botón 0 está en la lista de imágenes cero (AHIM \[ 0 \] ) con el índice de 1.</span><span class="sxs-lookup"><span data-stu-id="b0068-137">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="b0068-138">El botón 1 está en la lista de imágenes uno (AHIM \[ 1 \] ) con un índice de 1.</span><span class="sxs-lookup"><span data-stu-id="b0068-138">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="b0068-139">El botón 2 se encuentra en la lista de imágenes dos (AHIM \[ 2 \] ) con un índice de 1.</span><span class="sxs-lookup"><span data-stu-id="b0068-139">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="b0068-140">El botón 3 está en la lista de imágenes cero (AHIM \[ 0 \] ) con un índice de 2.</span><span class="sxs-lookup"><span data-stu-id="b0068-140">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="b0068-141">El botón 4 está en la lista de imágenes uno (AHIM \[ 1 \] ) con un índice de 3.</span><span class="sxs-lookup"><span data-stu-id="b0068-141">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="b0068-142">Por último, los botones se agregan al control de barra de herramientas con un mensaje [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="b0068-142">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="b0068-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0068-143">Requirements</span></span>



| <span data-ttu-id="b0068-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0068-144">Requirement</span></span> | <span data-ttu-id="b0068-145">Value</span><span class="sxs-lookup"><span data-stu-id="b0068-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0068-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0068-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b0068-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0068-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0068-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0068-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b0068-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0068-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0068-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0068-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0068-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0068-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0068-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0068-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0068-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0068-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

