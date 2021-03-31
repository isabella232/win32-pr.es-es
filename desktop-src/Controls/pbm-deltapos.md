---
title: Mensaje de PBM_DELTAPOS (commctrl. h)
description: Hace avanzar la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079563"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="757e7-104">Mensaje de DELTAPOS de PBM \_</span><span class="sxs-lookup"><span data-stu-id="757e7-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="757e7-105">Hace avanzar la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="757e7-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="757e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="757e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757e7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="757e7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="757e7-108">Cantidad que se va a avanzar la posición.</span><span class="sxs-lookup"><span data-stu-id="757e7-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="757e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="757e7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="757e7-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="757e7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757e7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="757e7-111">Return value</span></span>

<span data-ttu-id="757e7-112">Devuelve la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="757e7-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="757e7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="757e7-113">Remarks</span></span>

<span data-ttu-id="757e7-114">Si el incremento da como resultado un valor fuera del intervalo del control, la posición se establece en el límite más cercano.</span><span class="sxs-lookup"><span data-stu-id="757e7-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="757e7-115">El comportamiento de este mensaje es indefinido si se envía a un control que tiene el estilo [**de \_ marquesina de PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="757e7-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="757e7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757e7-116">Requirements</span></span>



| <span data-ttu-id="757e7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="757e7-117">Requirement</span></span> | <span data-ttu-id="757e7-118">Value</span><span class="sxs-lookup"><span data-stu-id="757e7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="757e7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="757e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="757e7-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="757e7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="757e7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="757e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="757e7-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="757e7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="757e7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="757e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="757e7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="757e7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





