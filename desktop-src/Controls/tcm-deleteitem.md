---
title: Mensaje de TCM_DELETEITEM (commctrl. h)
description: Quita un elemento de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996966"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="74195-105">Mensaje de TCM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="74195-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="74195-106">Quita un elemento de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="74195-106">Removes an item from a tab control.</span></span> <span data-ttu-id="74195-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="74195-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74195-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74195-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74195-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74195-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74195-110">Índice del elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="74195-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="74195-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74195-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74195-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="74195-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74195-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74195-113">Return value</span></span>

<span data-ttu-id="74195-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="74195-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74195-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74195-115">Requirements</span></span>



| <span data-ttu-id="74195-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="74195-116">Requirement</span></span> | <span data-ttu-id="74195-117">Value</span><span class="sxs-lookup"><span data-stu-id="74195-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74195-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74195-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74195-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74195-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74195-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74195-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74195-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74195-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74195-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74195-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="74195-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74195-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





