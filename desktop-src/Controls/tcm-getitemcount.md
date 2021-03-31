---
title: Mensaje de TCM_GETITEMCOUNT (commctrl. h)
description: Recupera el número de pestañas del control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150973"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="0b6a1-105">\_Mensaje GETITEMCOUNT de TCM</span><span class="sxs-lookup"><span data-stu-id="0b6a1-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="0b6a1-106">Recupera el número de pestañas del control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="0b6a1-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="0b6a1-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b6a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b6a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b6a1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b6a1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b6a1-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0b6a1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b6a1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0b6a1-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b6a1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b6a1-113">Return value</span></span>

<span data-ttu-id="0b6a1-114">Devuelve el número de elementos si se realiza correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6a1-115">Requirements</span></span>



| <span data-ttu-id="0b6a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6a1-116">Requirement</span></span> | <span data-ttu-id="0b6a1-117">Value</span><span class="sxs-lookup"><span data-stu-id="0b6a1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6a1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6a1-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0b6a1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b6a1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6a1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b6a1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b6a1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b6a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b6a1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b6a1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





