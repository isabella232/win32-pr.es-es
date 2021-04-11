---
title: Mensaje de EM_SETTABSTOPS (Winuser. h)
description: El \_ mensaje SETTABSTOPS em establece las tabulaciones en un control de edición multilínea.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150463"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="eb430-104">\_Mensaje SETTABSTOPS em</span><span class="sxs-lookup"><span data-stu-id="eb430-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="eb430-105">El **mensaje \_ SETTABSTOPS em** establece las tabulaciones en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="eb430-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="eb430-106">Cuando se copia texto en el control, cualquier carácter de tabulación del texto hace que se genere espacio hasta la siguiente tabulación.</span><span class="sxs-lookup"><span data-stu-id="eb430-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="eb430-107">Este mensaje solo lo procesan los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="eb430-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="eb430-108">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="eb430-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb430-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb430-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb430-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb430-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb430-111">Número de tabulaciones contenidas en la matriz.</span><span class="sxs-lookup"><span data-stu-id="eb430-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="eb430-112">Si este parámetro es cero, el parámetro *lParam* se omite y las tabulaciones predeterminadas se establecen en cada unidad de plantilla de cuadro de diálogo 32.</span><span class="sxs-lookup"><span data-stu-id="eb430-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="eb430-113">Si este parámetro es 1, las tabulaciones se establecen en cada *n* unidades de plantilla de cuadro de diálogo, donde *n* es la distancia a la que apunta el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="eb430-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="eb430-114">Si este parámetro es mayor que 1, *lParam* es un puntero a una matriz de puntos de tabulación.</span><span class="sxs-lookup"><span data-stu-id="eb430-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="eb430-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb430-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb430-116">Puntero a una matriz de enteros sin signo que especifican las tabulaciones, en unidades de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb430-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="eb430-117">Si el parámetro *wParam* es 1, este parámetro es un puntero a un entero sin signo que contiene la distancia entre todas las tabulaciones, en unidades de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb430-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb430-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb430-118">Return value</span></span>

<span data-ttu-id="eb430-119">Si se establecen todas las pestañas, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb430-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="eb430-120">Si no se establecen todas las pestañas, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="eb430-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb430-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb430-121">Remarks</span></span>

<span data-ttu-id="eb430-122">El **mensaje \_ SETTABSTOPS em** no vuelve a dibujar automáticamente la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="eb430-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="eb430-123">Si la aplicación está cambiando las tabulaciones del texto que ya está en el control de edición, debe llamar a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para volver a dibujar la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="eb430-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="eb430-124">Los valores especificados en la matriz se encuentran en unidades de plantilla de cuadro de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb430-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="eb430-125">Para convertir las medidas de las unidades de plantilla de cuadro de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="eb430-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="eb430-126">**Edición enriquecida:** Compatible con Microsoft Rich Edit 3,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eb430-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="eb430-127">Un control Rich Edit puede tener el número máximo de tabulaciones especificado por las tabulaciones MAX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="eb430-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="eb430-128">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="eb430-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb430-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb430-129">Requirements</span></span>



| <span data-ttu-id="eb430-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb430-130">Requirement</span></span> | <span data-ttu-id="eb430-131">Value</span><span class="sxs-lookup"><span data-stu-id="eb430-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb430-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb430-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb430-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eb430-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb430-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb430-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb430-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb430-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb430-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb430-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb430-137"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb430-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb430-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb430-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb430-139">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="eb430-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eb430-140">**InvalidateRect**</span><span class="sxs-lookup"><span data-stu-id="eb430-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="eb430-141">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="eb430-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

