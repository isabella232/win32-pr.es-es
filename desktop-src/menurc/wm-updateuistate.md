---
title: Mensaje de WM_UPDATEUISTATE (Winuser. h)
description: Una aplicación envía el mensaje de UPDATEUISTATE de WM \_ para cambiar el estado de la interfaz de usuario de la ventana especificada y de todas sus ventanas secundarias.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151210"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="9c1e7-104">Mensaje de UPDATEUISTATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="9c1e7-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="9c1e7-105">Una aplicación envía el mensaje de **\_ UPDATEUISTATE de WM** para cambiar el estado de la interfaz de usuario de la ventana especificada y de todas sus ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="9c1e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c1e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1e7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c1e7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1e7-108">La palabra de orden inferior especifica la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="9c1e7-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9c1e7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9c1e7-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="9c1e7-111">Significado</span><span class="sxs-lookup"><span data-stu-id="9c1e7-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="9c1e7-112"><dt>**Ius \_ BORRAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="9c1e7-113">El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe estar oculto.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="9c1e7-114"><dt>**Ius \_ INICIALIZAr**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="9c1e7-115">El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe cambiarse según el último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="9c1e7-116">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="9c1e7-117"><dt>**Ius \_ ESTABLECER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="9c1e7-118">El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe estar visible.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="9c1e7-119">La palabra de orden superior especifica qué elementos de estado de la interfaz de usuario se ven afectados o el estilo del control.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="9c1e7-120">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9c1e7-121">Value</span><span class="sxs-lookup"><span data-stu-id="9c1e7-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="9c1e7-122">Significado</span><span class="sxs-lookup"><span data-stu-id="9c1e7-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="9c1e7-123"><dt>**UISF \_**</dt> <dt>0x4</dt> activo</span><span class="sxs-lookup"><span data-stu-id="9c1e7-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="9c1e7-124">Un control debe dibujarse en el estilo utilizado para los controles activos.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="9c1e7-125"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="9c1e7-126">Aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="9c1e7-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="9c1e7-128">Indicadores de foco.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="9c1e7-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c1e7-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1e7-130">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c1e7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c1e7-131">Remarks</span></span>

<span data-ttu-id="9c1e7-132">Una ventana debe enviar este mensaje para cambiar el estado de la interfaz de usuario de todas sus ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="9c1e7-133">A diferencia del mensaje [**de \_ CHANGEUISTATE de WM**](wm-changeuistate.md) , que es una notificación, cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa el mensaje de **\_ UPDATEUISTATE de WM** , cambia el estado de la interfaz de usuario y propaga los cambios a todas las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="9c1e7-134">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) actualiza el estado de la interfaz de usuario según el valor de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9c1e7-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="9c1e7-135">Si se modifica el estado de la interfaz de usuario, la función envía el mensaje a todas las ventanas secundarias inmediatas.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="9c1e7-136">**DefWindowProc** también envía este mensaje cuando recibe un mensaje [**de \_ CHANGEUISTATE de WM**](wm-changeuistate.md) que notifica al sistema que una ventana secundaria intenta modificar el estado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9c1e7-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c1e7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c1e7-137">Requirements</span></span>



| <span data-ttu-id="9c1e7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1e7-138">Requirement</span></span> | <span data-ttu-id="9c1e7-139">Value</span><span class="sxs-lookup"><span data-stu-id="9c1e7-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1e7-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c1e7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1e7-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9c1e7-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c1e7-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c1e7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1e7-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c1e7-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c1e7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c1e7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c1e7-145"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e7-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c1e7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c1e7-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c1e7-147">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9c1e7-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c1e7-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9c1e7-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9c1e7-149">**CHANGEUISTATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9c1e7-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="9c1e7-150">**QUERYUISTATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9c1e7-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="9c1e7-151">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9c1e7-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c1e7-152">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="9c1e7-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

