---
title: Mensaje de TCM_HIGHLIGHTITEM (commctrl. h)
description: Establece el estado de resaltado de un elemento de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905544"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="08151-105">\_Mensaje HIGHLIGHTITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="08151-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="08151-106">Establece el estado de resaltado de un elemento de ficha.</span><span class="sxs-lookup"><span data-stu-id="08151-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="08151-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .</span><span class="sxs-lookup"><span data-stu-id="08151-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="08151-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08151-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08151-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08151-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08151-110">Valor **int** que especifica el índice de base cero de un elemento de control de ficha.</span><span class="sxs-lookup"><span data-stu-id="08151-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="08151-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08151-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08151-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **booleano** que especifica el estado de resaltado que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="08151-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="08151-113">Si este valor es **true**, la pestaña se resalta; Si es **false**, la pestaña se establece en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08151-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="08151-114">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="08151-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08151-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08151-115">Return value</span></span>

<span data-ttu-id="08151-116">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="08151-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08151-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08151-117">Remarks</span></span>

<span data-ttu-id="08151-118">En Comctl32.dll versión 6,0, este mensaje no tiene ningún efecto visible cuando un tema está activo.</span><span class="sxs-lookup"><span data-stu-id="08151-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="08151-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08151-119">Requirements</span></span>



| <span data-ttu-id="08151-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="08151-120">Requirement</span></span> | <span data-ttu-id="08151-121">Value</span><span class="sxs-lookup"><span data-stu-id="08151-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08151-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08151-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08151-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08151-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08151-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08151-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08151-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="08151-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08151-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08151-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="08151-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08151-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

