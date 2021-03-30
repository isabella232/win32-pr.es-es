---
title: Mensaje de TVM_GETIMAGELIST (commctrl. h)
description: Recupera el identificador de la lista de imágenes normal o de estado asociada a un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetImageList de TreeView.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803692"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="670ce-105">\_Mensaje de GETIMAGELIST TVM</span><span class="sxs-lookup"><span data-stu-id="670ce-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="670ce-106">Recupera el identificador de la lista de imágenes normal o de estado asociada a un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="670ce-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="670ce-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetImageList de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="670ce-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="670ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="670ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670ce-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="670ce-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="670ce-110">Tipo de lista de imágenes que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="670ce-110">Type of image list to retrieve.</span></span> <span data-ttu-id="670ce-111">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="670ce-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="670ce-112">Value</span><span class="sxs-lookup"><span data-stu-id="670ce-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="670ce-113">Significado</span><span class="sxs-lookup"><span data-stu-id="670ce-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="670ce-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="670ce-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="670ce-115">Indica la lista de imágenes normal, que contiene imágenes seleccionadas, no seleccionadas y superpuestas para los elementos de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="670ce-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="670ce-116"><dt>**Estado de TVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="670ce-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="670ce-117">Indica la lista de imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="670ce-117">Indicates the state image list.</span></span> <span data-ttu-id="670ce-118">Puede usar imágenes de estado para indicar los Estados de los elementos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="670ce-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="670ce-119">Se muestra una imagen de estado a la izquierda de la imagen seleccionada o no seleccionada de un elemento.</span><span class="sxs-lookup"><span data-stu-id="670ce-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="670ce-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="670ce-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="670ce-121">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="670ce-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670ce-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="670ce-122">Return value</span></span>

<span data-ttu-id="670ce-123">Devuelve un identificador HIMAGELIST a la lista de imágenes especificada.</span><span class="sxs-lookup"><span data-stu-id="670ce-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="670ce-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670ce-124">Requirements</span></span>



| <span data-ttu-id="670ce-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="670ce-125">Requirement</span></span> | <span data-ttu-id="670ce-126">Value</span><span class="sxs-lookup"><span data-stu-id="670ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="670ce-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="670ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="670ce-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="670ce-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="670ce-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="670ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="670ce-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="670ce-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="670ce-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="670ce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="670ce-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="670ce-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670ce-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="670ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670ce-134">**TVM \_ SETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="670ce-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





