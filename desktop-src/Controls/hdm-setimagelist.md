---
title: Mensaje de HDM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetImageList o header \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996333"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="c4517-105">HDM \_ SETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="c4517-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="c4517-106">Asigna una lista de imágenes a un control de encabezado existente.</span><span class="sxs-lookup"><span data-stu-id="c4517-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="c4517-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) o [**Header \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .</span><span class="sxs-lookup"><span data-stu-id="c4517-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4517-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4517-108">Parameters</span></span>

<dl> <span data-ttu-id="c4517-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="c4517-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="c4517-110">Uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c4517-110">One of the following values:</span></span>

| <span data-ttu-id="c4517-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c4517-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="c4517-112">Significado</span><span class="sxs-lookup"><span data-stu-id="c4517-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="c4517-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="c4517-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="c4517-114">Indica que se trata de una lista de imágenes normal.</span><span class="sxs-lookup"><span data-stu-id="c4517-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="c4517-115"><dt>**Estado de HDSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4517-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="c4517-116">Indica que se trata de una lista de imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="c4517-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="c4517-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4517-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4517-118">Identificador de una lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="c4517-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4517-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4517-119">Return value</span></span>

<span data-ttu-id="c4517-120">Devuelve el identificador de la lista de imágenes asociada previamente al control.</span><span class="sxs-lookup"><span data-stu-id="c4517-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="c4517-121">Devuelve **null** si se produce un error o si no se estableció ninguna lista de imágenes previamente.</span><span class="sxs-lookup"><span data-stu-id="c4517-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4517-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4517-122">Requirements</span></span>



| <span data-ttu-id="c4517-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4517-123">Requirement</span></span> | <span data-ttu-id="c4517-124">Value</span><span class="sxs-lookup"><span data-stu-id="c4517-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4517-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4517-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c4517-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c4517-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4517-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4517-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c4517-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4517-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4517-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4517-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4517-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4517-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





