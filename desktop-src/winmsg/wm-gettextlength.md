---
description: Determina la longitud, en caracteres, del texto asociado a una ventana.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Mensaje de WM_GETTEXTLENGTH (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002385"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="17437-103">Mensaje de GETTEXTLENGTH de WM \_</span><span class="sxs-lookup"><span data-stu-id="17437-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="17437-104">Determina la longitud, en caracteres, del texto asociado a una ventana.</span><span class="sxs-lookup"><span data-stu-id="17437-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="17437-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17437-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17437-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17437-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17437-107">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17437-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="17437-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17437-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17437-109">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17437-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17437-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17437-110">Return value</span></span>

<span data-ttu-id="17437-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="17437-111">Type: **LRESULT**</span></span>

<span data-ttu-id="17437-112">El valor devuelto es la longitud del texto en caracteres, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="17437-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="17437-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17437-113">Remarks</span></span>

<span data-ttu-id="17437-114">Para un control de edición, el texto que se va a copiar es el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="17437-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="17437-115">En el caso de un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="17437-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="17437-116">En el caso de un botón, el texto es el nombre del botón.</span><span class="sxs-lookup"><span data-stu-id="17437-116">For a button, the text is the button name.</span></span> <span data-ttu-id="17437-117">Para otras ventanas, el texto es el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="17437-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="17437-118">Para determinar la longitud de un elemento en un cuadro de lista, una aplicación puede usar el mensaje [**lb \_ GETTEXTLEN**](../controls/lb-gettextlen.md) .</span><span class="sxs-lookup"><span data-stu-id="17437-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="17437-119">Cuando se envía el mensaje de **\_ GETTEXTLENGTH de WM** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve la longitud, en caracteres, del texto.</span><span class="sxs-lookup"><span data-stu-id="17437-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="17437-120">En determinadas condiciones, la función **DefWindowProc** devuelve un valor que es mayor que la longitud real del texto.</span><span class="sxs-lookup"><span data-stu-id="17437-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="17437-121">Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto.</span><span class="sxs-lookup"><span data-stu-id="17437-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="17437-122">Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por tanto, se puede usar siempre para guiar la asignación de búfer.</span><span class="sxs-lookup"><span data-stu-id="17437-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="17437-123">Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.</span><span class="sxs-lookup"><span data-stu-id="17437-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="17437-124">Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)o [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) , o la función [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="17437-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="17437-125">El envío de un mensaje de **WM \_ GETTEXTLENGTH** a un control estático que no sea de texto, como un mapa de bits estático o un icono estático controlc, no devuelve un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="17437-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="17437-126">En su lugar, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="17437-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="17437-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17437-127">Requirements</span></span>



| <span data-ttu-id="17437-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="17437-128">Requirement</span></span> | <span data-ttu-id="17437-129">Value</span><span class="sxs-lookup"><span data-stu-id="17437-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17437-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17437-130">Minimum supported client</span></span><br/> | <span data-ttu-id="17437-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="17437-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17437-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17437-132">Minimum supported server</span></span><br/> | <span data-ttu-id="17437-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17437-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17437-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17437-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="17437-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17437-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17437-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="17437-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="17437-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="17437-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17437-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="17437-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="17437-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="17437-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="17437-140">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="17437-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="17437-141">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="17437-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="17437-142">**Vista**</span><span class="sxs-lookup"><span data-stu-id="17437-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17437-143">Windows</span><span class="sxs-lookup"><span data-stu-id="17437-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="17437-144">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="17437-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="17437-145">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="17437-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="17437-146">**\_apgettext GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="17437-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="17437-147">**LB \_ GETTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="17437-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
