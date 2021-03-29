---
title: Mensaje de TCM_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador de una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905548"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="c30aa-105">\_Mensaje GETITEMRECT de TCM</span><span class="sxs-lookup"><span data-stu-id="c30aa-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="c30aa-106">Recupera el rectángulo delimitador de una pestaña en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="c30aa-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="c30aa-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="c30aa-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c30aa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c30aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c30aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c30aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c30aa-110">Índice de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="c30aa-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="c30aa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c30aa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c30aa-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la pestaña, en coordenadas de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="c30aa-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c30aa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c30aa-113">Return value</span></span>

<span data-ttu-id="c30aa-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c30aa-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c30aa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c30aa-115">Requirements</span></span>



| <span data-ttu-id="c30aa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30aa-116">Requirement</span></span> | <span data-ttu-id="c30aa-117">Value</span><span class="sxs-lookup"><span data-stu-id="c30aa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c30aa-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c30aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c30aa-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c30aa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c30aa-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c30aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c30aa-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c30aa-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c30aa-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c30aa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c30aa-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c30aa-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

