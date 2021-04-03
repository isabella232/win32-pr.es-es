---
title: Mensaje de TBM_SETPOS (commctrl. h)
description: Establece la posición lógica actual del control deslizante en una barra de desplazamiento.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS controles de mensajes de Windows
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
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997139"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="28cd8-104">TBM \_ SETPOS</span><span class="sxs-lookup"><span data-stu-id="28cd8-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="28cd8-105">Establece la posición lógica actual del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="28cd8-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="28cd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28cd8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28cd8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28cd8-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="28cd8-108">Redraw flag.</span></span> <span data-ttu-id="28cd8-109">Si este parámetro es **true**, el mensaje vuelve a dibujar el control con el control deslizante en la posición especificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="28cd8-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="28cd8-110">Si este parámetro es **false**, el mensaje no vuelve a dibujar el control deslizante en la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="28cd8-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="28cd8-111">Tenga en cuenta que el mensaje establece el valor de la posición del control deslizante (tal y como lo devuelve el mensaje [**\_ GETPOS de TBM**](tbm-getpos.md) ), independientemente del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="28cd8-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="28cd8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28cd8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28cd8-113">Nueva posición lógica del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="28cd8-113">New logical position of the slider.</span></span> <span data-ttu-id="28cd8-114">Las posiciones lógicas válidas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="28cd8-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="28cd8-115">Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.</span><span class="sxs-lookup"><span data-stu-id="28cd8-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28cd8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28cd8-116">Return value</span></span>

<span data-ttu-id="28cd8-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28cd8-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28cd8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28cd8-118">Requirements</span></span>



| <span data-ttu-id="28cd8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28cd8-119">Requirement</span></span> | <span data-ttu-id="28cd8-120">Value</span><span class="sxs-lookup"><span data-stu-id="28cd8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28cd8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28cd8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28cd8-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28cd8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28cd8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28cd8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28cd8-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28cd8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28cd8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28cd8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28cd8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28cd8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





