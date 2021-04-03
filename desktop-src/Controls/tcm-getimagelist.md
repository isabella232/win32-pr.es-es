---
title: Mensaje de TCM_GETIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes asociada a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905549"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="d0308-105">\_Mensaje GETIMAGELIST de TCM</span><span class="sxs-lookup"><span data-stu-id="d0308-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="d0308-106">Recupera la lista de imágenes asociada a un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="d0308-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="d0308-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="d0308-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0308-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0308-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0308-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0308-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d0308-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d0308-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d0308-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0308-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d0308-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d0308-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0308-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0308-113">Return value</span></span>

<span data-ttu-id="d0308-114">Devuelve el identificador de la lista de imágenes si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d0308-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0308-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0308-115">Requirements</span></span>



| <span data-ttu-id="d0308-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0308-116">Requirement</span></span> | <span data-ttu-id="d0308-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0308-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0308-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0308-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0308-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0308-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0308-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0308-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0308-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0308-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0308-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0308-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0308-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0308-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





