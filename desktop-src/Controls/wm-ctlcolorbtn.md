---
title: Mensaje de WM_CTLCOLORBTN (Winuser. h)
description: El \_ mensaje de CTLCOLORBTN de WM se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y de fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995921"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="bb7d8-106">Mensaje de CTLCOLORBTN de WM \_</span><span class="sxs-lookup"><span data-stu-id="bb7d8-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="bb7d8-107">El mensaje de **\_ CTLCOLORBTN de WM** se envía a la ventana primaria de un botón antes de dibujar el botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="bb7d8-108">La ventana primaria puede cambiar los colores de texto y de fondo del botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="bb7d8-109">Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bb7d8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb7d8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7d8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb7d8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d8-112">**HDC** que especifica el identificador del contexto de presentación para el botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb7d8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d8-114">**HWnd** que especifica el identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7d8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb7d8-115">Return value</span></span>

<span data-ttu-id="bb7d8-116">Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="bb7d8-117">El sistema utiliza el pincel para pintar el fondo del botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7d8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb7d8-118">Remarks</span></span>

<span data-ttu-id="bb7d8-119">Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="bb7d8-120">Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="bb7d8-121">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el botón.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="bb7d8-122">Los botones con los estilos de [**\_ pulsador BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) no usan el pincel devuelto.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="bb7d8-123">Los botones con estos estilos siempre se dibujan con los colores del sistema predeterminados.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="bb7d8-124">Dibujar botones de reenvío requiere varios pinceles diferentes: la esfera, el resaltado y la sombra, pero el mensaje de **\_ CTLCOLORBTN de WM** permite que solo se devuelva un pincel.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="bb7d8-125">Para proporcionar una apariencia personalizada para botones de tecla de reenvío, use un botón dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="bb7d8-126">Para obtener más información, vea [crear controles de Owner-Drawn](user-controls-intro.md).</span><span class="sxs-lookup"><span data-stu-id="bb7d8-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="bb7d8-127">El mensaje de **\_ CTLCOLORBTN de WM** nunca se envía entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="bb7d8-128">Solo se envía dentro de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-128">It is sent only within one thread.</span></span>

<span data-ttu-id="bb7d8-129">El color del texto de una casilla o un botón de radio se aplica al cuadro o botón, su marca de verificación y el texto.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="bb7d8-130">El rectángulo de foco de estos botones sigue siendo el color predeterminado del sistema (normalmente negro).</span><span class="sxs-lookup"><span data-stu-id="bb7d8-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="bb7d8-131">El color de texto de un cuadro de grupo se aplica al texto, pero no a la línea que define el cuadro.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="bb7d8-132">El color del texto de un botón de la tecla de reenvío solo se aplica a su rectángulo de foco; no afecta al color del texto.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="bb7d8-133">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="bb7d8-134">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bb7d8-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="bb7d8-135">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="bb7d8-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7d8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb7d8-136">Requirements</span></span>



| <span data-ttu-id="bb7d8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7d8-137">Requirement</span></span> | <span data-ttu-id="bb7d8-138">Value</span><span class="sxs-lookup"><span data-stu-id="bb7d8-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7d8-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb7d8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7d8-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb7d8-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb7d8-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb7d8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7d8-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb7d8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb7d8-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb7d8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb7d8-144"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb7d8-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7d8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb7d8-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb7d8-146">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="bb7d8-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7d8-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="bb7d8-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="bb7d8-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="bb7d8-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

