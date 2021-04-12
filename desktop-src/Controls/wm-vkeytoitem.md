---
title: Mensaje de WM_VKEYTOITEM (Winuser. h)
description: Enviado por un cuadro de lista con el \_ estilo lb WANTKEYBOARDINPUT a su propietario en respuesta a un \_ mensaje de KEYDOWN de WM.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104361945"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="d0bc2-104">Mensaje de VKEYTOITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="d0bc2-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="d0bc2-105">Enviado por un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="d0bc2-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d0bc2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0bc2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0bc2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0bc2-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el código de tecla virtual de la clave que el usuario presionó.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="d0bc2-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="d0bc2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0bc2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0bc2-111">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0bc2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0bc2-112">Return value</span></span>

<span data-ttu-id="d0bc2-113">El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="d0bc2-114">Un valor devuelto de-2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna acción adicional por parte del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="d0bc2-115">(Vea la sección comentarios). Un valor devuelto de-1 indica que el cuadro de lista debe realizar la acción predeterminada en respuesta a la pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="d0bc2-116">Un valor devuelto de 0 o superior especifica el índice de un elemento del cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada de la pulsación de tecla en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0bc2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0bc2-117">Remarks</span></span>

<span data-ttu-id="d0bc2-118">Un valor devuelto de-2 solo es válido para las claves que el control de cuadro de lista no traduce en caracteres.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="d0bc2-119">Si el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) se convierte en un mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) y la aplicación procesa el mensaje de **\_ VKEYTOITEM de WM** generado como resultado de la pulsación de tecla, el cuadro de lista omite el valor devuelto y realiza el procesamiento predeterminado para ese carácter.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="d0bc2-120">**WM \_** Los mensajes KEYDOWN generados por claves como VK \_ up, VK \_ Down, VK \_ Next y VK \_ Previous no se traducen a mensajes de tipo **\_ Char** .</span><span class="sxs-lookup"><span data-stu-id="d0bc2-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="d0bc2-121">En tales casos, al interceptar el mensaje de **\_ VKEYTOITEM de WM** y devolver-2 se impide que el cuadro de lista realice el procesamiento predeterminado de esa clave.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="d0bc2-122">Para interceptar las claves que generan un mensaje Char y realizar un procesamiento especial, la aplicación debe crear una subclase del cuadro de lista, interceptar los mensajes de tipo [**\_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y de [**WM \_ Char**](/windows/desktop/inputdev/wm-char) y procesar los mensajes correctamente en el procedimiento de la subclase.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="d0bc2-123">Los comentarios anteriores se aplican a los cuadros de lista normales que se crean con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d0bc2-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="d0bc2-124">Si el cuadro de lista está dibujado por el propietario, la aplicación debe procesar el mensaje de [**\_ CHARTOITEM de WM**](wm-chartoitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d0bc2-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="d0bc2-125">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="d0bc2-126">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="d0bc2-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="d0bc2-127">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="d0bc2-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0bc2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0bc2-128">Requirements</span></span>



| <span data-ttu-id="d0bc2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0bc2-129">Requirement</span></span> | <span data-ttu-id="d0bc2-130">Value</span><span class="sxs-lookup"><span data-stu-id="d0bc2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0bc2-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0bc2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d0bc2-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0bc2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0bc2-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0bc2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d0bc2-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0bc2-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0bc2-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0bc2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0bc2-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0bc2-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0bc2-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0bc2-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0bc2-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d0bc2-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0bc2-139">**CHARTOITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d0bc2-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="d0bc2-140">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d0bc2-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d0bc2-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0bc2-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d0bc2-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0bc2-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d0bc2-143">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d0bc2-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

