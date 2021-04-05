---
description: Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Mensaje de WM_GETTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815454"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="9af3c-103">\_Mensaje GETTEXT de WM</span><span class="sxs-lookup"><span data-stu-id="9af3c-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="9af3c-104">Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9af3c-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="9af3c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9af3c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af3c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9af3c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af3c-107">Número máximo de caracteres que se van a copiar, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="9af3c-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="9af3c-108">Las aplicaciones ANSI pueden tener el tamaño de la cadena en el búfer reducido (a un mínimo de la mitad del valor de *wParam* ) debido a la conversión de ANSI a Unicode.</span><span class="sxs-lookup"><span data-stu-id="9af3c-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="9af3c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9af3c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af3c-110">Puntero al búfer que va a recibir el texto.</span><span class="sxs-lookup"><span data-stu-id="9af3c-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af3c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9af3c-111">Return value</span></span>

<span data-ttu-id="9af3c-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9af3c-112">Type: **LRESULT**</span></span>

<span data-ttu-id="9af3c-113">El valor devuelto es el número de caracteres copiados, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="9af3c-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af3c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9af3c-114">Remarks</span></span>

<span data-ttu-id="9af3c-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia el texto asociado a la ventana en el búfer especificado y devuelve el número de caracteres copiados.</span><span class="sxs-lookup"><span data-stu-id="9af3c-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="9af3c-116">Tenga en cuenta que para los controles estáticos que no son de texto, proporciona el texto con el que se creó originalmente el control, es decir, el número de identificación.</span><span class="sxs-lookup"><span data-stu-id="9af3c-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="9af3c-117">Sin embargo, proporciona el identificador del control estático de no texto como se creó originalmente.</span><span class="sxs-lookup"><span data-stu-id="9af3c-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="9af3c-118">Es decir, si usa posteriormente un **STM \_ SETIMAGE** para cambiarlo, el identificador original se seguiría devolviendo.</span><span class="sxs-lookup"><span data-stu-id="9af3c-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="9af3c-119">Para un control de edición, el texto que se va a copiar es el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="9af3c-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="9af3c-120">En el caso de un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="9af3c-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="9af3c-121">En el caso de un botón, el texto es el nombre del botón.</span><span class="sxs-lookup"><span data-stu-id="9af3c-121">For a button, the text is the button name.</span></span> <span data-ttu-id="9af3c-122">Para otras ventanas, el texto es el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9af3c-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="9af3c-123">Para copiar el texto de un elemento en un cuadro de lista, una aplicación puede usar el mensaje [**lb \_ GETTEXT**](../controls/lb-gettext.md) .</span><span class="sxs-lookup"><span data-stu-id="9af3c-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="9af3c-124">Cuando el mensaje de **\_ GETTEXT GETTEXT** se envía a un control estático con el estilo de **\_ icono de SS** , se devolverá un identificador al icono en los primeros cuatro bytes del búfer al que apunta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="9af3c-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="9af3c-125">Esto solo es aplicable si se ha utilizado el mensaje de [**WM \_ SETTEXT**](wm-settext.md) para establecer el icono.</span><span class="sxs-lookup"><span data-stu-id="9af3c-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="9af3c-126">**Edición enriquecida:** Si el texto que se va a copiar es superior a 64 k, use el mensaje [**em \_ STREAMOUT**](../controls/em-streamout.md) o [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="9af3c-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="9af3c-127">El envío de un mensaje **\_ GETTEXT de WM** a un control estático que no sea de texto, como un mapa de bits estático o un control de icono estático, no devuelve un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="9af3c-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="9af3c-128">En su lugar, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9af3c-128">Instead, it returns zero.</span></span> <span data-ttu-id="9af3c-129">Además, en las primeras versiones de Windows, las aplicaciones pueden enviar un mensaje de **\_ GETTEXT de WM** a un control estático que no es de texto para recuperar el identificador del control.</span><span class="sxs-lookup"><span data-stu-id="9af3c-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="9af3c-130">Para recuperar el identificador de un control, las aplicaciones pueden usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) pasando **GWL \_ ID** como valor de índice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mediante el **\_ identificador de GWLP**.</span><span class="sxs-lookup"><span data-stu-id="9af3c-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af3c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af3c-131">Requirements</span></span>



| <span data-ttu-id="9af3c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af3c-132">Requirement</span></span> | <span data-ttu-id="9af3c-133">Value</span><span class="sxs-lookup"><span data-stu-id="9af3c-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af3c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af3c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9af3c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9af3c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9af3c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af3c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9af3c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9af3c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9af3c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9af3c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af3c-139"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9af3c-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af3c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af3c-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="9af3c-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9af3c-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9af3c-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9af3c-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9af3c-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="9af3c-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="9af3c-144">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="9af3c-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="9af3c-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="9af3c-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="9af3c-146">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="9af3c-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="9af3c-147">**GETTEXTLENGTH de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9af3c-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="9af3c-148">**SETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9af3c-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="9af3c-149">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9af3c-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9af3c-150">Windows</span><span class="sxs-lookup"><span data-stu-id="9af3c-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="9af3c-151">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9af3c-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9af3c-152">**\_GETSELTEXT em**</span><span class="sxs-lookup"><span data-stu-id="9af3c-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="9af3c-153">**\_STREAMOUT em**</span><span class="sxs-lookup"><span data-stu-id="9af3c-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="9af3c-154">**\_apgettext GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="9af3c-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
