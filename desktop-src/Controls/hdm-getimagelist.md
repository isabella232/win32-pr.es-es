---
title: Mensaje de HDM_GETIMAGELIST (commctrl. h)
description: Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetImageList o header \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802858"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="affcb-105">HDM \_ GETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="affcb-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="affcb-106">Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente.</span><span class="sxs-lookup"><span data-stu-id="affcb-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="affcb-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) o [**Header \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) .</span><span class="sxs-lookup"><span data-stu-id="affcb-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="affcb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="affcb-108">Parameters</span></span>

<dl> <span data-ttu-id="affcb-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="affcb-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="affcb-110">Uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="affcb-110">One of the following values:</span></span>

| <span data-ttu-id="affcb-111">Valor</span><span class="sxs-lookup"><span data-stu-id="affcb-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="affcb-112">Significado</span><span class="sxs-lookup"><span data-stu-id="affcb-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="affcb-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="affcb-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="affcb-114">Indica que se trata de una lista de imágenes normal.</span><span class="sxs-lookup"><span data-stu-id="affcb-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="affcb-115"><dt>**Estado de HDSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="affcb-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="affcb-116">Indica que se trata de una lista de imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="affcb-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="affcb-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="affcb-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="affcb-118">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="affcb-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="affcb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="affcb-119">Return value</span></span>

<span data-ttu-id="affcb-120">Devuelve un identificador para el conjunto de lista de imágenes para el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="affcb-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="affcb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="affcb-121">Requirements</span></span>



| <span data-ttu-id="affcb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="affcb-122">Requirement</span></span> | <span data-ttu-id="affcb-123">Value</span><span class="sxs-lookup"><span data-stu-id="affcb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="affcb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="affcb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="affcb-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="affcb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="affcb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="affcb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="affcb-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="affcb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="affcb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="affcb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="affcb-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="affcb-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





