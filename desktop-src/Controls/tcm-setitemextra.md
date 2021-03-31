---
title: Mensaje de TCM_SETITEMEXTRA (commctrl. h)
description: Establece el número de bytes por pestaña reservado para los datos definidos por la aplicación en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149881"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="0aa18-105">\_Mensaje SETITEMEXTRA de TCM</span><span class="sxs-lookup"><span data-stu-id="0aa18-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="0aa18-106">Establece el número de bytes por pestaña reservado para los datos definidos por la aplicación en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="0aa18-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="0aa18-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .</span><span class="sxs-lookup"><span data-stu-id="0aa18-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0aa18-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aa18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa18-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aa18-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa18-110">Número de bytes adicionales.</span><span class="sxs-lookup"><span data-stu-id="0aa18-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0aa18-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aa18-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0aa18-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0aa18-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa18-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aa18-113">Return value</span></span>

<span data-ttu-id="0aa18-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0aa18-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa18-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aa18-115">Remarks</span></span>

<span data-ttu-id="0aa18-116">De forma predeterminada, el número de bytes adicionales es cuatro.</span><span class="sxs-lookup"><span data-stu-id="0aa18-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="0aa18-117">Una aplicación que cambia el número de bytes adicionales no puede usar la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar y establecer los datos definidos por la aplicación para una pestaña. En su lugar, debe definir una nueva estructura que conste de la estructura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguido de los miembros definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0aa18-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="0aa18-118">Una aplicación solo debe cambiar el número de bytes adicionales cuando un control de ficha no contiene ninguna pestaña.</span><span class="sxs-lookup"><span data-stu-id="0aa18-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa18-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa18-119">Requirements</span></span>



| <span data-ttu-id="0aa18-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa18-120">Requirement</span></span> | <span data-ttu-id="0aa18-121">Value</span><span class="sxs-lookup"><span data-stu-id="0aa18-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa18-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa18-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa18-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0aa18-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0aa18-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa18-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa18-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0aa18-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0aa18-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa18-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa18-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa18-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





