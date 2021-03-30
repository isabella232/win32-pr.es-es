---
title: Mensaje de TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Establece los estilos extendidos que usará el control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079394"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="d256f-105">\_Mensaje SETEXTENDEDSTYLE de TCM</span><span class="sxs-lookup"><span data-stu-id="d256f-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d256f-106">Establece los estilos extendidos que usará el control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="d256f-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="d256f-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="d256f-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d256f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d256f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d256f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d256f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d256f-110">Valor **DWORD** que indica qué estilos de *lParam* se van a ver afectados.</span><span class="sxs-lookup"><span data-stu-id="d256f-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="d256f-111">Solo se cambiarán los estilos extendidos de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d256f-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="d256f-112">Todos los demás estilos se conservarán tal como están.</span><span class="sxs-lookup"><span data-stu-id="d256f-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="d256f-113">Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="d256f-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="d256f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d256f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d256f-115">Valor que especifica los estilos de control de pestaña extendido.</span><span class="sxs-lookup"><span data-stu-id="d256f-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="d256f-116">Este valor es una combinación de [estilos extendidos](tab-control-extended-styles.md)de control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="d256f-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d256f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d256f-117">Return value</span></span>

<span data-ttu-id="d256f-118">Devuelve un valor **DWORD** que contiene los estilos extendidos del control de pestaña anterior.</span><span class="sxs-lookup"><span data-stu-id="d256f-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="d256f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d256f-119">Remarks</span></span>

<span data-ttu-id="d256f-120">El parámetro *wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes.</span><span class="sxs-lookup"><span data-stu-id="d256f-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="d256f-121">Por ejemplo, si pasa los [**ect \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **TCS \_ ex \_ FLATSEPARATORS** , pero el resto de los estilos permanecerán iguales.</span><span class="sxs-lookup"><span data-stu-id="d256f-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="d256f-122">Por motivos de compatibilidad con versiones anteriores, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) no se ha actualizado para usar *dwExMask*.</span><span class="sxs-lookup"><span data-stu-id="d256f-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d256f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d256f-123">Requirements</span></span>



| <span data-ttu-id="d256f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d256f-124">Requirement</span></span> | <span data-ttu-id="d256f-125">Value</span><span class="sxs-lookup"><span data-stu-id="d256f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d256f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d256f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d256f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d256f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d256f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d256f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d256f-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d256f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d256f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d256f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d256f-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d256f-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d256f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d256f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d256f-133">**\_GETEXTENDEDSTYLE TCM**</span><span class="sxs-lookup"><span data-stu-id="d256f-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





