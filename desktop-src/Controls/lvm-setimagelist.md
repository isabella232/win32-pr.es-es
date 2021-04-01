---
title: Mensaje de LVM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetImageList de ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995934"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="55e31-105">\_Mensaje SETIMAGELIST LVM</span><span class="sxs-lookup"><span data-stu-id="55e31-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="55e31-106">Asigna una lista de imágenes a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="55e31-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="55e31-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="55e31-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="55e31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55e31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55e31-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e31-110">Tipo de lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="55e31-110">Type of image list.</span></span> <span data-ttu-id="55e31-111">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="55e31-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="55e31-112">Value</span><span class="sxs-lookup"><span data-stu-id="55e31-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="55e31-113">Significado</span><span class="sxs-lookup"><span data-stu-id="55e31-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="55e31-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="55e31-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="55e31-115">Lista de imágenes con iconos grandes.</span><span class="sxs-lookup"><span data-stu-id="55e31-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="55e31-116"><dt>**LVSIL \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="55e31-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="55e31-117">Lista de imágenes con iconos pequeños.</span><span class="sxs-lookup"><span data-stu-id="55e31-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="55e31-118"><dt>**Estado de LVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55e31-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="55e31-119">Lista de imágenes con imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="55e31-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="55e31-120"><dt>**LVSIL \_ encabezadodelgrupo**</dt></span><span class="sxs-lookup"><span data-stu-id="55e31-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="55e31-121">Lista de imágenes para el encabezado de grupo.</span><span class="sxs-lookup"><span data-stu-id="55e31-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="55e31-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55e31-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e31-123">Identificador de la lista de imágenes que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="55e31-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55e31-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55e31-124">Return value</span></span>

<span data-ttu-id="55e31-125">Devuelve el identificador de la lista de imágenes asociada previamente al control si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="55e31-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e31-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55e31-126">Remarks</span></span>

<span data-ttu-id="55e31-127">La lista de imágenes actual se destruirá cuando se destruya el control de vista de lista, a menos que se establezca el estilo [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="55e31-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="55e31-128">Si usa este mensaje para reemplazar una lista de imágenes por otra, la aplicación debe destruir explícitamente todas las listas de imágenes distintas de la actual.</span><span class="sxs-lookup"><span data-stu-id="55e31-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e31-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55e31-129">Requirements</span></span>



| <span data-ttu-id="55e31-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="55e31-130">Requirement</span></span> | <span data-ttu-id="55e31-131">Value</span><span class="sxs-lookup"><span data-stu-id="55e31-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e31-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55e31-132">Minimum supported client</span></span><br/> | <span data-ttu-id="55e31-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55e31-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55e31-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55e31-134">Minimum supported server</span></span><br/> | <span data-ttu-id="55e31-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="55e31-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55e31-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55e31-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="55e31-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e31-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





