---
title: Mensaje de LVM_GETIMAGELIST (commctrl. h)
description: Recupera el identificador de una lista de imágenes que se usa para dibujar los elementos de la vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetImageList de ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150543"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="6a342-105">\_Mensaje GETIMAGELIST LVM</span><span class="sxs-lookup"><span data-stu-id="6a342-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="6a342-106">Recupera el identificador de una lista de imágenes que se usa para dibujar los elementos de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="6a342-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="6a342-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="6a342-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a342-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a342-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a342-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a342-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a342-110">Lista de imágenes que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6a342-110">Image list to retrieve.</span></span> <span data-ttu-id="6a342-111">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="6a342-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="6a342-112">Value</span><span class="sxs-lookup"><span data-stu-id="6a342-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="6a342-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6a342-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="6a342-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="6a342-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="6a342-115">Lista de imágenes con iconos grandes.</span><span class="sxs-lookup"><span data-stu-id="6a342-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="6a342-116"><dt>**LVSIL \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="6a342-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="6a342-117">Lista de imágenes con iconos pequeños.</span><span class="sxs-lookup"><span data-stu-id="6a342-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="6a342-118"><dt>**Estado de LVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a342-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="6a342-119">Lista de imágenes con imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="6a342-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="6a342-120"><dt>**LVSIL \_ encabezadodelgrupo**</dt></span><span class="sxs-lookup"><span data-stu-id="6a342-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="6a342-121">Lista de imágenes para el encabezado de grupo.</span><span class="sxs-lookup"><span data-stu-id="6a342-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="6a342-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a342-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6a342-123">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6a342-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a342-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a342-124">Return value</span></span>

<span data-ttu-id="6a342-125">Devuelve el identificador de la lista de imágenes especificada si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6a342-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a342-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a342-126">Requirements</span></span>



| <span data-ttu-id="6a342-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a342-127">Requirement</span></span> | <span data-ttu-id="6a342-128">Value</span><span class="sxs-lookup"><span data-stu-id="6a342-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a342-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a342-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a342-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a342-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a342-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a342-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a342-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a342-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a342-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a342-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a342-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a342-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





