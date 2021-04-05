---
title: Mensaje de TCM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- TCM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078850"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="4dcb0-105">\_Mensaje SETIMAGELIST de TCM</span><span class="sxs-lookup"><span data-stu-id="4dcb0-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="4dcb0-106">Asigna una lista de imágenes a un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="4dcb0-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="4dcb0-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="4dcb0-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dcb0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dcb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dcb0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dcb0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4dcb0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4dcb0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4dcb0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dcb0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dcb0-112">Identificador de la lista de imágenes que se va a asignar al control de ficha.</span><span class="sxs-lookup"><span data-stu-id="4dcb0-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dcb0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dcb0-113">Return value</span></span>

<span data-ttu-id="4dcb0-114">Devuelve el identificador de la lista de imágenes anterior o **null** si no hay ninguna lista de imágenes anterior.</span><span class="sxs-lookup"><span data-stu-id="4dcb0-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dcb0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dcb0-115">Requirements</span></span>



| <span data-ttu-id="4dcb0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dcb0-116">Requirement</span></span> | <span data-ttu-id="4dcb0-117">Value</span><span class="sxs-lookup"><span data-stu-id="4dcb0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dcb0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dcb0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4dcb0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4dcb0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dcb0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dcb0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4dcb0-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dcb0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dcb0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dcb0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dcb0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dcb0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





