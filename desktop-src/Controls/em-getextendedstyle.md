---
title: Mensaje de EM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera el estilo extendido de un control de edición. Envíe este mensaje explícitamente o mediante la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491813"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="2f068-105">Mensaje de EM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="2f068-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="2f068-106">Recupera el estilo extendido para un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="2f068-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="2f068-107">Envíe este mensaje explícitamente o mediante la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="2f068-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f068-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f068-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f068-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f068-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f068-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f068-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f068-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f068-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f068-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f068-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f068-113">Return value</span></span>

<span data-ttu-id="2f068-114">Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2f068-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f068-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f068-115">Remarks</span></span>

<span data-ttu-id="2f068-116">Los estilos extendidos para un control de edición no tienen nada que hacer con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="2f068-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f068-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f068-117">Requirements</span></span>



| <span data-ttu-id="2f068-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f068-118">Requirement</span></span> | <span data-ttu-id="2f068-119">Value</span><span class="sxs-lookup"><span data-stu-id="2f068-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f068-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f068-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f068-121">Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f068-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f068-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f068-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f068-123">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f068-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f068-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f068-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f068-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f068-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

