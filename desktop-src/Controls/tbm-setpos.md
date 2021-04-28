---
title: TBM_SETPOS mensaje (Commctrl.h)
description: 'TBM_SETPOS mensaje: establece la posición lógica actual del control deslizante en una barra de seguimiento.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS de mensajes controles de Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085873"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="eea55-104">Mensaje TBM \_ SETPOS</span><span class="sxs-lookup"><span data-stu-id="eea55-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="eea55-105">Establece la posición lógica actual del control deslizante en una barra de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="eea55-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="eea55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eea55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea55-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eea55-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eea55-108">Volver a dibujar la marca.</span><span class="sxs-lookup"><span data-stu-id="eea55-108">Redraw flag.</span></span> <span data-ttu-id="eea55-109">Si este parámetro es **TRUE,** el mensaje vuelve a dibujar el control con el control deslizante en la posición dada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="eea55-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="eea55-110">Si este parámetro es **FALSE,** el mensaje no vuelve a dibujar el control deslizante en la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="eea55-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="eea55-111">Tenga en cuenta que el mensaje establece el valor de la posición del control deslizante (tal como lo devuelve el mensaje [**\_ GETPOS de TBM)**](tbm-getpos.md) independientemente del *parámetro wParam.*</span><span class="sxs-lookup"><span data-stu-id="eea55-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="eea55-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eea55-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eea55-113">Nueva posición lógica del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="eea55-113">New logical position of the slider.</span></span> <span data-ttu-id="eea55-114">Las posiciones lógicas válidas son los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="eea55-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="eea55-115">Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.</span><span class="sxs-lookup"><span data-stu-id="eea55-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea55-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eea55-116">Return value</span></span>

<span data-ttu-id="eea55-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eea55-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea55-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea55-118">Requirements</span></span>



| <span data-ttu-id="eea55-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea55-119">Requirement</span></span> | <span data-ttu-id="eea55-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eea55-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eea55-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eea55-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eea55-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eea55-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eea55-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eea55-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eea55-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eea55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea55-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="eea55-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





