---
title: Mensaje de TCM_SETCURSEL (commctrl. h)
description: Selecciona una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetCurSel.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996420"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="5cc97-105">\_Mensaje SETCURSEL de TCM</span><span class="sxs-lookup"><span data-stu-id="5cc97-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="5cc97-106">Selecciona una pestaña en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="5cc97-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="5cc97-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="5cc97-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cc97-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cc97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc97-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cc97-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cc97-110">Índice de la pestaña que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="5cc97-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="5cc97-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cc97-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5cc97-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5cc97-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc97-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cc97-113">Return value</span></span>

<span data-ttu-id="5cc97-114">Devuelve el índice de la pestaña seleccionada anteriormente si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5cc97-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc97-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cc97-115">Remarks</span></span>

<span data-ttu-id="5cc97-116">Un control de ficha no envía un código de notificación [TCN \_ SELCHANGING](tcn-selchanging.md) o [TCN \_ SELCHANGE](tcn-selchange.md) cuando se selecciona una ficha con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5cc97-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc97-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc97-117">Requirements</span></span>



| <span data-ttu-id="5cc97-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc97-118">Requirement</span></span> | <span data-ttu-id="5cc97-119">Value</span><span class="sxs-lookup"><span data-stu-id="5cc97-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc97-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc97-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc97-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc97-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cc97-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc97-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc97-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc97-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc97-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cc97-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc97-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc97-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





