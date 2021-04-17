---
title: Mensaje de MCM_SETMONTHDELTA (commctrl. h)
description: Establece la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658373"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="5050e-106">Mensaje de MCM \_ SETMONTHDELTA</span><span class="sxs-lookup"><span data-stu-id="5050e-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="5050e-107">Establece la tasa de desplazamiento para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="5050e-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="5050e-108">La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="5050e-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="5050e-109">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="5050e-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5050e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5050e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5050e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5050e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5050e-112">Valor que representa el número de meses que se va a establecer como la tasa de desplazamiento del control.</span><span class="sxs-lookup"><span data-stu-id="5050e-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="5050e-113">Si este valor es cero, la diferencia de mes se restablece en el valor predeterminado, que es el número de meses que se muestran en el control.</span><span class="sxs-lookup"><span data-stu-id="5050e-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="5050e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5050e-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5050e-115">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5050e-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5050e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5050e-116">Return value</span></span>

<span data-ttu-id="5050e-117">Devuelve un valor INT que representa la tasa de desplazamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="5050e-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="5050e-118">Si la tasa de desplazamiento no se estableció previamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="5050e-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5050e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5050e-119">Remarks</span></span>

<span data-ttu-id="5050e-120">Las teclas Re Pág y Av Pág, VK \_ anterior y VK \_ Next, cambian el mes seleccionado en uno, independientemente del número de meses que se muestren o del valor establecido por **MCM \_ SETMONTHDELTA**.</span><span class="sxs-lookup"><span data-stu-id="5050e-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5050e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5050e-121">Requirements</span></span>



| <span data-ttu-id="5050e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5050e-122">Requirement</span></span> | <span data-ttu-id="5050e-123">Value</span><span class="sxs-lookup"><span data-stu-id="5050e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5050e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5050e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5050e-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5050e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5050e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5050e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5050e-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5050e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5050e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5050e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5050e-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5050e-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





