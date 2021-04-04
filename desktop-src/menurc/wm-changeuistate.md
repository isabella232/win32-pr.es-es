---
title: Mensaje de WM_CHANGEUISTATE (Winuser. h)
description: Una aplicación envía el mensaje de CHANGEUISTATE de WM \_ para indicar que se debe cambiar el estado de la interfaz de usuario.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803836"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="ca850-104">Mensaje de CHANGEUISTATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="ca850-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="ca850-105">Una aplicación envía el mensaje de **\_ CHANGEUISTATE de WM** para indicar que se debe cambiar el estado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca850-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="ca850-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca850-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca850-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca850-108">La palabra de orden inferior especifica la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="ca850-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="ca850-109">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ca850-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="ca850-110">Value</span><span class="sxs-lookup"><span data-stu-id="ca850-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="ca850-111">Significado</span><span class="sxs-lookup"><span data-stu-id="ca850-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="ca850-112"><dt>**Ius \_ BORRAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="ca850-113">Las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior deben estar desactivadas.</span><span class="sxs-lookup"><span data-stu-id="ca850-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="ca850-114"><dt>**Ius \_ INICIALIZAr**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="ca850-115">Las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior deben cambiarse en función del último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca850-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="ca850-116">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ca850-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="ca850-117"><dt>**Ius \_ ESTABLECER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="ca850-118">Se deben establecer las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="ca850-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="ca850-119">La palabra de orden superior especifica qué elementos de estado de la interfaz de usuario se ven afectados o el estilo del control.</span><span class="sxs-lookup"><span data-stu-id="ca850-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="ca850-120">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ca850-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="ca850-121">Value</span><span class="sxs-lookup"><span data-stu-id="ca850-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="ca850-122">Significado</span><span class="sxs-lookup"><span data-stu-id="ca850-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="ca850-123"><dt>**UISF \_**</dt> <dt>0x4</dt> activo</span><span class="sxs-lookup"><span data-stu-id="ca850-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="ca850-124">Un control debe dibujarse en el estilo utilizado para los controles activos.</span><span class="sxs-lookup"><span data-stu-id="ca850-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="ca850-125"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="ca850-126">Los aceleradores de teclado están ocultos.</span><span class="sxs-lookup"><span data-stu-id="ca850-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="ca850-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="ca850-128">Los indicadores de foco están ocultos.</span><span class="sxs-lookup"><span data-stu-id="ca850-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="ca850-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca850-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca850-130">Este parámetro no se utiliza y debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="ca850-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca850-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca850-131">Remarks</span></span>

<span data-ttu-id="ca850-132">Una ventana debe enviar este mensaje a sí mismo o a su elemento primario cuando debe cambiar los elementos de estado de la interfaz de usuario de todas las ventanas de la misma jerarquía.</span><span class="sxs-lookup"><span data-stu-id="ca850-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="ca850-133">El procedimiento de ventana debe permitir que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procese este mensaje para que todo el árbol de la ventana tenga un estado de interfaz de usuario coherente.</span><span class="sxs-lookup"><span data-stu-id="ca850-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="ca850-134">Cuando la ventana de nivel superior recibe el mensaje de **\_ CHANGEUISTATE de WM** , envía un mensaje de [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con los mismos parámetros a todas las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="ca850-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="ca850-135">Cuando el sistema procesa el mensaje de **\_ UPDATEUISTATE de WM** , realiza el cambio en el estado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca850-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="ca850-136">Si la palabra de orden inferior de *wParam* es \_ Initialize Initialize, el sistema enviará el mensaje de [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con un estado de IU basado en el último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca850-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="ca850-137">Por ejemplo, si la última entrada procedía del mouse, el sistema ocultará las señales de teclado. Y, si la última entrada procede del teclado, el sistema mostrará las señales de teclado. Si el estado resultante del procesamiento de **WM \_ CHANGEUISTATE** es el mismo que el anterior, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca850-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca850-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca850-138">Requirements</span></span>



| <span data-ttu-id="ca850-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca850-139">Requirement</span></span> | <span data-ttu-id="ca850-140">Value</span><span class="sxs-lookup"><span data-stu-id="ca850-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca850-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca850-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ca850-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ca850-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ca850-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca850-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ca850-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca850-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca850-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca850-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca850-146"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca850-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca850-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca850-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca850-148">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ca850-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="ca850-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca850-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ca850-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca850-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca850-151">**QUERYUISTATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ca850-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="ca850-152">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ca850-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca850-153">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="ca850-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

