---
description: Se produce cuando el usuario suelta un botón del mouse mientras el mouse está sobre el control InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit. MouseUp (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c331ec5dd0dd6a39ec956eda6980ee02cddd298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278860"
---
# <a name="inkeditmouseup-event"></a><span data-ttu-id="4c64d-103">Evento InkEdit. MouseUp</span><span class="sxs-lookup"><span data-stu-id="4c64d-103">InkEdit.MouseUp event</span></span>

<span data-ttu-id="4c64d-104">Se produce cuando el usuario suelta un botón del mouse mientras el mouse está sobre el control [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4c64d-104">Occurs when the user releases a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c64d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c64d-105">Syntax</span></span>


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="4c64d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c64d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c64d-107">*Botón*</span><span class="sxs-lookup"><span data-stu-id="4c64d-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="4c64d-108">Miembro de la enumeración [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica qué botones del mouse se han liberado.</span><span class="sxs-lookup"><span data-stu-id="4c64d-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were released.</span></span>



| <span data-ttu-id="4c64d-109">Value</span><span class="sxs-lookup"><span data-stu-id="4c64d-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="4c64d-110">Significado</span><span class="sxs-lookup"><span data-stu-id="4c64d-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="4c64d-111"><dt>**No \_ BOTÓN** de</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="4c64d-112">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4c64d-112">Default.</span></span> <span data-ttu-id="4c64d-113">No se presionó ningún botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="4c64d-114"><dt>**Izquierda \_ BOTÓN** de</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="4c64d-115">Se presionó el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="4c64d-116"><dt>**Derecha \_ BOTÓN** de</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="4c64d-117">Se presionó el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="4c64d-118"><dt>**Centro \_ BOTÓN** de</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="4c64d-119">Se presionó el botón central del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="4c64d-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="4c64d-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="4c64d-121">Miembro de la enumeración [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras están presionadas en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4c64d-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="4c64d-122">Value</span><span class="sxs-lookup"><span data-stu-id="4c64d-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="4c64d-123">Significado</span><span class="sxs-lookup"><span data-stu-id="4c64d-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="4c64d-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="4c64d-125">Especifica que la tecla Mayús se utilizó como modificador.</span><span class="sxs-lookup"><span data-stu-id="4c64d-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="4c64d-126"><dt>**IKM \_ Control** de</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="4c64d-127">Especifica que la tecla CTRL se utilizó como modificador.</span><span class="sxs-lookup"><span data-stu-id="4c64d-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="4c64d-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="4c64d-129">Especifica que la tecla ALT se ha utilizado como modificador.</span><span class="sxs-lookup"><span data-stu-id="4c64d-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="4c64d-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="4c64d-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="4c64d-131">Coordenada x actual, en píxeles, del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="4c64d-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="4c64d-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="4c64d-133">La coordenada y actual, en píxeles, del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="4c64d-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c64d-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c64d-134">Return value</span></span>

<span data-ttu-id="4c64d-135">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4c64d-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c64d-136">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c64d-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c64d-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c64d-137">Remarks</span></span>

<span data-ttu-id="4c64d-138">Si se presiona un botón del mouse mientras el puntero se encuentra sobre un control [InkEdit](inkedit-control-reference.md) , ese control captura el mouse y recibe todos los eventos del mouse hasta el último evento **MouseUp** incluido.</span><span class="sxs-lookup"><span data-stu-id="4c64d-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last **MouseUp** event.</span></span> <span data-ttu-id="4c64d-139">Esto implica que las coordenadas del puntero del mouse (x, y) devueltas por un evento del mouse pueden no estar siempre en el área interna del objeto que los recibe.</span><span class="sxs-lookup"><span data-stu-id="4c64d-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="4c64d-140">Si los botones del mouse se presionan sucesivamente, el objeto que captura el mouse después de la primera pulsada recibe todos los eventos del mouse hasta que se liberen todos los botones.</span><span class="sxs-lookup"><span data-stu-id="4c64d-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="4c64d-141">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="4c64d-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="4c64d-142">La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeMouseUp.</span><span class="sxs-lookup"><span data-stu-id="4c64d-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c64d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c64d-143">Requirements</span></span>



| <span data-ttu-id="4c64d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c64d-144">Requirement</span></span> | <span data-ttu-id="4c64d-145">Value</span><span class="sxs-lookup"><span data-stu-id="4c64d-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c64d-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c64d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4c64d-147">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c64d-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c64d-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c64d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4c64d-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4c64d-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4c64d-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c64d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c64d-151"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c64d-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c64d-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c64d-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c64d-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4c64d-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c64d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c64d-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="4c64d-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4c64d-156">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="4c64d-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="4c64d-157">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="4c64d-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="4c64d-158">[**Control InkEdit de eventos MouseDown \[\]**](inkedit-mousedown.md)</span><span class="sxs-lookup"><span data-stu-id="4c64d-158">[**MouseDown Event \[InkEdit Control\]**](inkedit-mousedown.md)</span></span>
</dt> <dt>

<span data-ttu-id="4c64d-159">[**Control InkEdit de eventos MouseMove \[\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="4c64d-159">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> </dl>

 

