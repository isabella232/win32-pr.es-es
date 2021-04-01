---
title: Mensaje de PBM_STEPIT (commctrl. h)
description: Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento del paso mediante el envío del mensaje de SETSTEP de PBM \_ .
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996732"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="0043a-105">Mensaje de STEPIT de PBM \_</span><span class="sxs-lookup"><span data-stu-id="0043a-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="0043a-106">Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="0043a-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="0043a-107">Una aplicación establece el incremento del paso mediante el envío del mensaje de [**\_ SETSTEP de PBM**](pbm-setstep.md) .</span><span class="sxs-lookup"><span data-stu-id="0043a-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="0043a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0043a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0043a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0043a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0043a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0043a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0043a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0043a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0043a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0043a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0043a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0043a-113">Return value</span></span>

<span data-ttu-id="0043a-114">Devuelve la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="0043a-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="0043a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0043a-115">Remarks</span></span>

<span data-ttu-id="0043a-116">Cuando la posición supera el valor de intervalo máximo, este mensaje restablece la posición actual para que el indicador de progreso vuelva a empezar desde el principio.</span><span class="sxs-lookup"><span data-stu-id="0043a-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="0043a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0043a-117">Requirements</span></span>



| <span data-ttu-id="0043a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0043a-118">Requirement</span></span> | <span data-ttu-id="0043a-119">Value</span><span class="sxs-lookup"><span data-stu-id="0043a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0043a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0043a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0043a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0043a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0043a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0043a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0043a-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0043a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0043a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0043a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0043a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0043a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





