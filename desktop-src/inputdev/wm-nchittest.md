---
title: Mensaje de WM_NCHITTEST (Winuser. h)
description: Se envía a una ventana para determinar qué parte de la ventana corresponde a una coordenada de pantalla determinada.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCHITTEST
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695898"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="9a582-104">Mensaje de NCHITTEST de WM \_</span><span class="sxs-lookup"><span data-stu-id="9a582-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="9a582-105">Se envía a una ventana para determinar qué parte de la ventana corresponde a una coordenada de pantalla determinada.</span><span class="sxs-lookup"><span data-stu-id="9a582-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="9a582-106">Esto puede ocurrir, por ejemplo, cuando se mueve el cursor, cuando se presiona o se suelta un botón del mouse o en respuesta a una llamada a una función como [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="9a582-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="9a582-107">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="9a582-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="9a582-108">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="9a582-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="9a582-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9a582-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="9a582-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a582-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a582-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a582-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a582-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9a582-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9a582-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a582-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a582-114">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="9a582-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="9a582-115">La coordenada es relativa a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9a582-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="9a582-116">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="9a582-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="9a582-117">La coordenada es relativa a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9a582-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a582-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a582-118">Return value</span></span>

<span data-ttu-id="9a582-119">El valor devuelto de la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) es uno de los siguientes valores, que indica la posición de la zona activa del cursor.</span><span class="sxs-lookup"><span data-stu-id="9a582-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="9a582-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a582-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="9a582-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a582-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a582-122"><dt>**HTBORDER**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="9a582-123">En el borde de una ventana que no tiene un borde de ajuste de tamaño.</span><span class="sxs-lookup"><span data-stu-id="9a582-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="9a582-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="9a582-125">En el borde inferior horizontal de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana verticalmente).</span><span class="sxs-lookup"><span data-stu-id="9a582-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="9a582-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="9a582-127">En la esquina inferior izquierda de un borde de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana en diagonal).</span><span class="sxs-lookup"><span data-stu-id="9a582-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="9a582-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="9a582-129">En la esquina inferior derecha de un borde de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana en diagonal).</span><span class="sxs-lookup"><span data-stu-id="9a582-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="9a582-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="9a582-131">En una barra de título.</span><span class="sxs-lookup"><span data-stu-id="9a582-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="9a582-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="9a582-133">En un área cliente.</span><span class="sxs-lookup"><span data-stu-id="9a582-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9a582-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="9a582-135">En un botón **cerrar** .</span><span class="sxs-lookup"><span data-stu-id="9a582-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="9a582-136"><dt>**HTERROR**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="9a582-137">En el fondo de la pantalla o en una línea divisoria entre ventanas (igual que **HTNOWHERE**, con la excepción de que la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un bip del sistema para indicar un error).</span><span class="sxs-lookup"><span data-stu-id="9a582-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="9a582-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="9a582-139">En un cuadro de tamaño (igual que **HTSIZE**).</span><span class="sxs-lookup"><span data-stu-id="9a582-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="9a582-140"><dt>**HTHELP**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="9a582-141">En un botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="9a582-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="9a582-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="9a582-143">En una barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="9a582-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="9a582-144"><dt>**HTLEFT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="9a582-145">En el borde izquierdo de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana horizontalmente).</span><span class="sxs-lookup"><span data-stu-id="9a582-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9a582-146"><dt>**HTMENU**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="9a582-147">En un menú.</span><span class="sxs-lookup"><span data-stu-id="9a582-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="9a582-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="9a582-149">En un botón **maximizar** .</span><span class="sxs-lookup"><span data-stu-id="9a582-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="9a582-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="9a582-151">En un botón **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="9a582-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="9a582-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="9a582-153">En el fondo de la pantalla o en una línea divisoria entre ventanas.</span><span class="sxs-lookup"><span data-stu-id="9a582-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="9a582-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="9a582-155">En un botón **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="9a582-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="9a582-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="9a582-157">En el borde derecho de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana horizontalmente).</span><span class="sxs-lookup"><span data-stu-id="9a582-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9a582-158"><dt>**HTSIZE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="9a582-159">En un cuadro de tamaño (igual que **HTGROWBOX**).</span><span class="sxs-lookup"><span data-stu-id="9a582-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="9a582-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="9a582-161">En un menú ventana o en un botón **cerrar** de una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9a582-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="9a582-162"><dt>**HTTOP**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="9a582-163">En el borde superior horizontal de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9a582-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="9a582-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="9a582-165">En la esquina superior izquierda de un borde de ventana.</span><span class="sxs-lookup"><span data-stu-id="9a582-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="9a582-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="9a582-167">En la esquina superior derecha de un borde de ventana.</span><span class="sxs-lookup"><span data-stu-id="9a582-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="9a582-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="9a582-169">En una ventana actualmente incluida en otra ventana del mismo subproceso (el mensaje se enviará a las ventanas subyacentes en el mismo subproceso hasta que uno de ellos devuelva un código que no sea **HTTRANSPARENT**).</span><span class="sxs-lookup"><span data-stu-id="9a582-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="9a582-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="9a582-171">En la barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="9a582-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="9a582-172"><dt>**HTZOOM**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="9a582-173">En un botón **maximizar** .</span><span class="sxs-lookup"><span data-stu-id="9a582-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="9a582-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a582-174">Remarks</span></span>

<span data-ttu-id="9a582-175">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="9a582-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="9a582-176">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="9a582-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="9a582-177">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9a582-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="9a582-178">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="9a582-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a582-179">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="9a582-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="9a582-180">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="9a582-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="9a582-181">**Windows Vista:** Al crear fotogramas personalizados que incluyen los botones de título estándar, este mensaje debe pasarse primero a la función [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="9a582-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="9a582-182">Esto permite que el Administrador de ventanas de escritorio (DWM) proporcione pruebas de posicionamiento para los botones de subtítulos.</span><span class="sxs-lookup"><span data-stu-id="9a582-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="9a582-183">Si **DwmDefWindowProc** no controla el mensaje, es posible que se necesite un procesamiento adicional de **\_ NCHITTEST de WM** .</span><span class="sxs-lookup"><span data-stu-id="9a582-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a582-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a582-184">Requirements</span></span>



| <span data-ttu-id="9a582-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a582-185">Requirement</span></span> | <span data-ttu-id="9a582-186">Value</span><span class="sxs-lookup"><span data-stu-id="9a582-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a582-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a582-187">Minimum supported client</span></span><br/> | <span data-ttu-id="9a582-188">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9a582-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a582-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a582-189">Minimum supported server</span></span><br/> | <span data-ttu-id="9a582-190">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a582-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a582-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a582-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a582-192"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a582-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a582-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a582-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a582-194">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9a582-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a582-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9a582-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9a582-196">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="9a582-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="9a582-197">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="9a582-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="9a582-198">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9a582-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9a582-199">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="9a582-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="9a582-200">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9a582-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9a582-201">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="9a582-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="9a582-202">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a582-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

