---
title: Mensaje de TCM_SETCURFOCUS (commctrl. h)
description: Establece el foco en una pestaña especificada de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996421"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="867e0-105">\_Mensaje SETCURFOCUS de TCM</span><span class="sxs-lookup"><span data-stu-id="867e0-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="867e0-106">Establece el foco en una pestaña especificada de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="867e0-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="867e0-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="867e0-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="867e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="867e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="867e0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="867e0-110">Índice de la pestaña que obtiene el foco.</span><span class="sxs-lookup"><span data-stu-id="867e0-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="867e0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="867e0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="867e0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="867e0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867e0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="867e0-113">Return value</span></span>

<span data-ttu-id="867e0-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="867e0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="867e0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="867e0-115">Remarks</span></span>

<span data-ttu-id="867e0-116">Si el control de pestaña tiene el estilo de [**\_ botones de TCS**](tab-control-styles.md) (modo de botón), la pestaña con el foco puede ser diferente de la pestaña seleccionada. Por ejemplo, cuando se selecciona una pestaña, el usuario puede presionar las teclas de dirección para establecer el foco en una pestaña diferente sin cambiar la pestaña seleccionada. En el modo de botón, **TCM \_ SETCURFOCUS** establece el foco de entrada en el botón asociado a la pestaña especificada, pero no cambia la pestaña seleccionada.</span><span class="sxs-lookup"><span data-stu-id="867e0-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="867e0-117">Si el control de pestañas no tiene el estilo de [**\_ botones de TCS**](tab-control-styles.md) , cambiar el foco también cambia la pestaña seleccionada. En este caso, el control de pestañas envía los códigos de notificación [TCN \_ SELCHANGING](tcn-selchanging.md) y [TCN \_ SELCHANGE](tcn-selchange.md) a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="867e0-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="867e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="867e0-118">Requirements</span></span>



| <span data-ttu-id="867e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="867e0-119">Requirement</span></span> | <span data-ttu-id="867e0-120">Value</span><span class="sxs-lookup"><span data-stu-id="867e0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="867e0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="867e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="867e0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="867e0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="867e0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="867e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="867e0-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="867e0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="867e0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="867e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="867e0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="867e0-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867e0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="867e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867e0-128">**\_GETCURFOCUS TCM**</span><span class="sxs-lookup"><span data-stu-id="867e0-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 





