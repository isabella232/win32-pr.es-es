---
title: Mensaje de WM_CHARTOITEM (Winuser. h)
description: Se envía mediante un cuadro de lista con el \_ estilo lb WANTKEYBOARDINPUT a su propietario en respuesta a un mensaje de tipo char de WM \_ .
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104362382"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="a25a7-104">Mensaje de CHARTOITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="a25a7-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="a25a7-105">Se envía mediante un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de tipo [**\_ Char de WM**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="a25a7-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a25a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a25a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25a7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a25a7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a25a7-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el código de carácter de la tecla que el usuario presionó.</span><span class="sxs-lookup"><span data-stu-id="a25a7-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="a25a7-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a25a7-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="a25a7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a25a7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a25a7-111">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a25a7-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a25a7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a25a7-112">Return value</span></span>

<span data-ttu-id="a25a7-113">El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="a25a7-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="a25a7-114">Un valor devuelto de-1 o-2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna otra acción por parte del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a25a7-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="a25a7-115">Un valor devuelto de 0 o superior especifica el índice de base cero de un elemento del cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada para la pulsación de tecla en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="a25a7-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="a25a7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a25a7-116">Remarks</span></span>

<span data-ttu-id="a25a7-117">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="a25a7-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="a25a7-118">Solo los cuadros de lista dibujados por el propietario que no tienen el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) pueden recibir este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a25a7-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="a25a7-119">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="a25a7-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="a25a7-120">Se omite el valor de *DWL \_ MSGRESULT* establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="a25a7-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25a7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a25a7-121">Requirements</span></span>



| <span data-ttu-id="a25a7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a25a7-122">Requirement</span></span> | <span data-ttu-id="a25a7-123">Value</span><span class="sxs-lookup"><span data-stu-id="a25a7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25a7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a25a7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a25a7-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a25a7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a25a7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a25a7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a25a7-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a25a7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a25a7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a25a7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a25a7-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a25a7-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25a7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a25a7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a25a7-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a25a7-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a25a7-132">**VKEYTOITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a25a7-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="a25a7-133">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a25a7-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a25a7-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a25a7-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="a25a7-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a25a7-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a25a7-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a25a7-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a25a7-137">**carácter de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a25a7-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

