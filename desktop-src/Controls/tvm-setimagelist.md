---
title: Mensaje de TVM_SETIMAGELIST (commctrl. h)
description: Establece la lista de imágenes normal o de estado de un control de vista de árbol y vuelve a dibujar el control mediante las nuevas imágenes. Puede enviar este mensaje explícitamente o mediante la \_ macro SetImageList de TreeView.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802317"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="56130-105">\_Mensaje de SETIMAGELIST TVM</span><span class="sxs-lookup"><span data-stu-id="56130-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="56130-106">Establece la lista de imágenes normal o de estado de un control de vista de árbol y vuelve a dibujar el control mediante las nuevas imágenes.</span><span class="sxs-lookup"><span data-stu-id="56130-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="56130-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetImageList de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="56130-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="56130-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56130-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56130-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56130-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56130-110">Tipo de lista de imágenes que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="56130-110">Type of image list to set.</span></span> <span data-ttu-id="56130-111">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="56130-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="56130-112">Value</span><span class="sxs-lookup"><span data-stu-id="56130-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="56130-113">Significado</span><span class="sxs-lookup"><span data-stu-id="56130-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="56130-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="56130-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="56130-115">Indica la lista de imágenes normal, que contiene imágenes seleccionadas, no seleccionadas y superpuestas para los elementos de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="56130-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="56130-116"><dt>**Estado de TVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56130-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="56130-117">Indica la lista de imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="56130-117">Indicates the state image list.</span></span> <span data-ttu-id="56130-118">Puede usar imágenes de estado para indicar los Estados de los elementos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56130-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="56130-119">Se muestra una imagen de estado a la izquierda de la imagen seleccionada o no seleccionada de un elemento.</span><span class="sxs-lookup"><span data-stu-id="56130-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56130-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56130-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56130-121">Identificador de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="56130-121">Handle to the image list.</span></span> <span data-ttu-id="56130-122">Si *lParam* es **null**, el mensaje quita la lista de imágenes especificada del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="56130-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56130-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56130-123">Return value</span></span>

<span data-ttu-id="56130-124">Devuelve el identificador de la lista de imágenes anterior, si existe, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="56130-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56130-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56130-125">Remarks</span></span>

<span data-ttu-id="56130-126">El control de vista de árbol no destruirá la lista de imágenes especificada con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="56130-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="56130-127">La aplicación debe destruir la lista de imágenes cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="56130-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="56130-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56130-128">Requirements</span></span>



| <span data-ttu-id="56130-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="56130-129">Requirement</span></span> | <span data-ttu-id="56130-130">Value</span><span class="sxs-lookup"><span data-stu-id="56130-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56130-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56130-131">Minimum supported client</span></span><br/> | <span data-ttu-id="56130-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56130-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56130-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56130-133">Minimum supported server</span></span><br/> | <span data-ttu-id="56130-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56130-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56130-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56130-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="56130-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56130-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56130-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="56130-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56130-138">**TVM \_ GETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="56130-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





