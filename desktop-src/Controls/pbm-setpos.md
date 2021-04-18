---
title: Mensaje de PBM_SETPOS (commctrl. h)
description: Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658265"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="b0818-104">Mensaje de SETPOS de PBM \_</span><span class="sxs-lookup"><span data-stu-id="b0818-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="b0818-105">Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="b0818-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0818-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0818-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0818-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0818-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0818-108">Entero con signo que se convierte en la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="b0818-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="b0818-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0818-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0818-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b0818-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0818-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0818-111">Return value</span></span>

<span data-ttu-id="b0818-112">Devuelve la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="b0818-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0818-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0818-113">Remarks</span></span>

<span data-ttu-id="b0818-114">Si *wParam* está fuera del intervalo del control, la posición se establece en el límite más cercano.</span><span class="sxs-lookup"><span data-stu-id="b0818-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="b0818-115">No envíe este mensaje a un control que tenga el estilo [**de \_ marquesina de PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b0818-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0818-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0818-116">Requirements</span></span>



| <span data-ttu-id="b0818-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0818-117">Requirement</span></span> | <span data-ttu-id="b0818-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0818-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0818-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0818-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0818-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0818-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0818-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0818-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0818-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0818-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0818-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0818-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0818-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0818-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





