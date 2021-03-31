---
title: Mensaje de TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea se debe mostrar en modo de marquesina.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151049"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="3301a-104">Mensaje de la \_ \_ barra de \_ progreso del conjunto de TDM \_</span><span class="sxs-lookup"><span data-stu-id="3301a-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="3301a-105">Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea se debe mostrar en modo de marquesina.</span><span class="sxs-lookup"><span data-stu-id="3301a-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="3301a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3301a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3301a-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3301a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3301a-108">Un **booleano** que indica si la barra de progreso se debe mostrar en modo de marquesina.</span><span class="sxs-lookup"><span data-stu-id="3301a-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="3301a-109">Un valor **true** activa el modo de marquesina y el valor **false** desactiva el modo de marquesina.</span><span class="sxs-lookup"><span data-stu-id="3301a-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="3301a-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3301a-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3301a-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3301a-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3301a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3301a-112">Return value</span></span>

<span data-ttu-id="3301a-113">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3301a-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3301a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3301a-114">Remarks</span></span>

<span data-ttu-id="3301a-115">Para obtener información sobre el modo de marquesina, vea [control de barra de progreso](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="3301a-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3301a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3301a-116">Requirements</span></span>



| <span data-ttu-id="3301a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3301a-117">Requirement</span></span> | <span data-ttu-id="3301a-118">Value</span><span class="sxs-lookup"><span data-stu-id="3301a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3301a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3301a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3301a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3301a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3301a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3301a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3301a-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3301a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3301a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3301a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3301a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3301a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





