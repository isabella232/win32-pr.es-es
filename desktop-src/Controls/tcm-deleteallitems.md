---
title: Mensaje de TCM_DELETEALLITEMS (commctrl. h)
description: Quita todos los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535122"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="81880-105">\_Mensaje DELETEALLITEMS de TCM</span><span class="sxs-lookup"><span data-stu-id="81880-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="81880-106">Quita todos los elementos de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="81880-106">Removes all items from a tab control.</span></span> <span data-ttu-id="81880-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="81880-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81880-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81880-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81880-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81880-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="81880-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="81880-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="81880-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81880-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="81880-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="81880-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81880-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81880-113">Return value</span></span>

<span data-ttu-id="81880-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="81880-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="81880-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81880-115">Requirements</span></span>



| <span data-ttu-id="81880-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="81880-116">Requirement</span></span> | <span data-ttu-id="81880-117">Value</span><span class="sxs-lookup"><span data-stu-id="81880-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81880-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81880-118">Minimum supported client</span></span><br/> | <span data-ttu-id="81880-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81880-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81880-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81880-120">Minimum supported server</span></span><br/> | <span data-ttu-id="81880-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="81880-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81880-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81880-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="81880-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81880-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





