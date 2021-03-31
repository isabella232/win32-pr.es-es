---
title: Mensaje de TTM_SETDELAYTIME (commctrl. h)
description: Establece las duraciones inicial, emergente y de presentación de un control ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996407"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="e0124-104">TTM \_ SETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="e0124-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="e0124-105">Establece las duraciones inicial, emergente y de presentación de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e0124-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0124-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0124-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0124-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0124-108">Marca que especifica el valor de tiempo que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="e0124-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="e0124-109">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e0124-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="e0124-110">Value</span><span class="sxs-lookup"><span data-stu-id="e0124-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="e0124-111">Significado</span><span class="sxs-lookup"><span data-stu-id="e0124-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="e0124-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="e0124-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="e0124-113">Establece la cantidad de tiempo que una ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta.</span><span class="sxs-lookup"><span data-stu-id="e0124-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="e0124-114">Para devolver el tiempo de retraso de autopop a su valor predeterminado, establezca *lParam* en-1.</span><span class="sxs-lookup"><span data-stu-id="e0124-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="e0124-115"><dt>**TTDT \_ inicial**</dt></span><span class="sxs-lookup"><span data-stu-id="e0124-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="e0124-116">Establece la cantidad de tiempo que un puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="e0124-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="e0124-117">Para devolver el tiempo de retraso inicial a su valor predeterminado, establezca *lParam* en-1.</span><span class="sxs-lookup"><span data-stu-id="e0124-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="e0124-118"><dt>**TTDT \_ Mostrar**</dt></span><span class="sxs-lookup"><span data-stu-id="e0124-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="e0124-119">Establezca la cantidad de tiempo que tardará en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se mueva de una herramienta a otra.</span><span class="sxs-lookup"><span data-stu-id="e0124-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="e0124-120">Para devolver el tiempo de retraso de la representación a su valor predeterminado, establezca *lParam* en-1.</span><span class="sxs-lookup"><span data-stu-id="e0124-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="e0124-121"><dt>**TTDT \_ automática**</dt></span><span class="sxs-lookup"><span data-stu-id="e0124-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="e0124-122">Establezca los tres tiempos de retraso en las proporciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="e0124-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="e0124-123">El tiempo de autopop será diez veces la hora inicial y el tiempo de la presentación será una quinta parte de la hora inicial.</span><span class="sxs-lookup"><span data-stu-id="e0124-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="e0124-124">Si se establece esta marca, use un valor positivo de *lParam* para especificar el tiempo inicial, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e0124-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="e0124-125">Establezca *lParam* en un valor negativo para devolver los tres tiempos de retardo a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="e0124-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0124-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0124-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0124-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el tiempo de retardo, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e0124-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="e0124-128">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e0124-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0124-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0124-129">Return value</span></span>

<span data-ttu-id="e0124-130">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e0124-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0124-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0124-131">Remarks</span></span>

<span data-ttu-id="e0124-132">Los tiempos de retraso predeterminados se basan en el tiempo de doble clic.</span><span class="sxs-lookup"><span data-stu-id="e0124-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="e0124-133">Para el tiempo de doble clic predeterminado de 500 ms, los tiempos de retardo inicial, autopop y de representación son 500 ms, 5.000 MS y 100M, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e0124-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="e0124-134">En el fragmento de código siguiente se usa la función [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) para determinar los tres tiempos de retraso de cualquier sistema.</span><span class="sxs-lookup"><span data-stu-id="e0124-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="e0124-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0124-135">Requirements</span></span>



| <span data-ttu-id="e0124-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0124-136">Requirement</span></span> | <span data-ttu-id="e0124-137">Value</span><span class="sxs-lookup"><span data-stu-id="e0124-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0124-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0124-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e0124-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0124-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0124-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0124-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e0124-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0124-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0124-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0124-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0124-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0124-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0124-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0124-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0124-145">**TTM \_ GETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="e0124-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 

