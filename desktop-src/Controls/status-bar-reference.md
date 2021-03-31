---
title: Barra de estado
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de estado.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794769"
---
# <a name="status-bar"></a><span data-ttu-id="7af9f-103">Barra de estado</span><span class="sxs-lookup"><span data-stu-id="7af9f-103">Status Bar</span></span>

<span data-ttu-id="7af9f-104">Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="7af9f-105">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="7af9f-105">Overviews</span></span>



| <span data-ttu-id="7af9f-106">Tema</span><span class="sxs-lookup"><span data-stu-id="7af9f-106">Topic</span></span>                          | <span data-ttu-id="7af9f-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="7af9f-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af9f-108">Barras de estado</span><span class="sxs-lookup"><span data-stu-id="7af9f-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="7af9f-109">Una *barra de estado* es una ventana horizontal situada en la parte inferior de una ventana primaria en la que una aplicación puede mostrar diversos tipos de información de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="7af9f-110">Functions</span><span class="sxs-lookup"><span data-stu-id="7af9f-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7af9f-111">Tema</span><span class="sxs-lookup"><span data-stu-id="7af9f-111">Topic</span></span></th>
<th><span data-ttu-id="7af9f-112">Contenido</span><span class="sxs-lookup"><span data-stu-id="7af9f-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7af9f-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="7af9f-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="7af9f-114">Crea una ventana de estado, que se utiliza normalmente para mostrar el estado de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7af9f-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="7af9f-115">La ventana aparece generalmente en la parte inferior de la ventana primaria y contiene el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7af9f-116">Esta función está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="7af9f-116">This function is obsolete.</span></span> <span data-ttu-id="7af9f-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7af9f-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7af9f-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="7af9f-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="7af9f-119">La función <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> dibuja el texto especificado en el estilo de una ventana de estado con bordes.</span><span class="sxs-lookup"><span data-stu-id="7af9f-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7af9f-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="7af9f-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="7af9f-121">Procesa <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> y <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensajes y muestra texto de ayuda sobre el menú actual en la ventana de estado especificada.</span><span class="sxs-lookup"><span data-stu-id="7af9f-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="7af9f-122">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="7af9f-122">Messages</span></span>



| <span data-ttu-id="7af9f-123">Tema</span><span class="sxs-lookup"><span data-stu-id="7af9f-123">Topic</span></span>                                               | <span data-ttu-id="7af9f-124">Contenido</span><span class="sxs-lookup"><span data-stu-id="7af9f-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af9f-125">**SB \_ GETBORDERS**</span><span class="sxs-lookup"><span data-stu-id="7af9f-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="7af9f-126">Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="7af9f-127">**SB \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="7af9f-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="7af9f-128">Recupera el icono de un elemento en una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="7af9f-129">**SB \_ GETPARTS**</span><span class="sxs-lookup"><span data-stu-id="7af9f-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="7af9f-130">Recupera un recuento de los elementos de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="7af9f-131">El mensaje también recupera la coordenada del borde derecho del número especificado de partes.</span><span class="sxs-lookup"><span data-stu-id="7af9f-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="7af9f-132">**SB \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="7af9f-133">Recupera el rectángulo delimitador de un elemento de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="7af9f-134">**GETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="7af9f-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="7af9f-135">El [**mensaje \_ GETTEXT de SB**](sb-gettext.md) recupera el texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="7af9f-136">**SB \_ GETTEXTLENGTH**</span><span class="sxs-lookup"><span data-stu-id="7af9f-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="7af9f-137">El [**mensaje \_ GETTEXTLENGTH de SB**](sb-gettextlength.md) recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="7af9f-138">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="7af9f-139">Recupera el texto de información sobre herramientas de un elemento de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="7af9f-140">La barra de estado se debe crear con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="7af9f-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="7af9f-141">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="7af9f-142">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="7af9f-143">**SB \_ ISSIMPLE**</span><span class="sxs-lookup"><span data-stu-id="7af9f-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="7af9f-144">Comprueba un control de barra de estado para determinar si está en modo simple.</span><span class="sxs-lookup"><span data-stu-id="7af9f-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="7af9f-145">**SB \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="7af9f-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="7af9f-146">Establece el color de fondo de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="7af9f-147">**SB \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="7af9f-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="7af9f-148">Establece el icono de un elemento en una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="7af9f-149">**SB \_ SETMINHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="7af9f-150">Establece el alto mínimo del área de dibujo de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="7af9f-151">**SB \_ SETPARTS**</span><span class="sxs-lookup"><span data-stu-id="7af9f-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="7af9f-152">Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.</span><span class="sxs-lookup"><span data-stu-id="7af9f-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="7af9f-153">**SETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="7af9f-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="7af9f-154">El \_ mensaje SETTEXT de SB establece el texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="7af9f-155">**SB \_ SETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="7af9f-156">Establece el texto de información sobre herramientas para un elemento de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7af9f-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="7af9f-157">La barra de estado se debe haber creado con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="7af9f-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="7af9f-158">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="7af9f-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="7af9f-159">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="7af9f-160">Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="7af9f-161">**SB \_ simple**</span><span class="sxs-lookup"><span data-stu-id="7af9f-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="7af9f-162">Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje [**\_ SETPARTS de SB**](sb-setparts.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="7af9f-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="7af9f-163">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="7af9f-163">Notifications</span></span>



| <span data-ttu-id="7af9f-164">Tema</span><span class="sxs-lookup"><span data-stu-id="7af9f-164">Topic</span></span>                                                 | <span data-ttu-id="7af9f-165">Contenido</span><span class="sxs-lookup"><span data-stu-id="7af9f-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af9f-166">NM \_ haga clic (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="7af9f-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="7af9f-167">Notifica a la ventana primaria de un control de barra de estado que el usuario ha pulsado el botón primario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="7af9f-168">[Nm \_ Haga clic en (barra de estado)](nm-click-status-bar.md) se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="7af9f-169">NM \_ DBLCLK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="7af9f-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="7af9f-170">Notifica a la ventana primaria de un control de barra de estado que el usuario ha haga doble clic en el botón primario del mouse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="7af9f-171">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="7af9f-172">NM \_ RCLICK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="7af9f-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="7af9f-173">Notifica a la ventana primaria de un control de barra de estado que el usuario ha hace clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="7af9f-174">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="7af9f-175">NM \_ RDBLCLK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="7af9f-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="7af9f-176">Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="7af9f-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="7af9f-177">[Nm \_ RDBLCLK (barra de estado)](nm-rdblclk-status-bar.md) se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="7af9f-178">SBN \_ SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="7af9f-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="7af9f-179">Lo envía un control de barra de estado cuando cambia el modo simple debido a un mensaje [**\_ simple de SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="7af9f-180">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af9f-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="7af9f-181">Constantes</span><span class="sxs-lookup"><span data-stu-id="7af9f-181">Constants</span></span>



| <span data-ttu-id="7af9f-182">Tema</span><span class="sxs-lookup"><span data-stu-id="7af9f-182">Topic</span></span>                                      | <span data-ttu-id="7af9f-183">Contenido</span><span class="sxs-lookup"><span data-stu-id="7af9f-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af9f-184">Estilos de barra de estado</span><span class="sxs-lookup"><span data-stu-id="7af9f-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="7af9f-185">En esta sección se enumeran los estilos, además de los estilos de ventana estándar, que admiten los controles de *barra de estado* .</span><span class="sxs-lookup"><span data-stu-id="7af9f-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

