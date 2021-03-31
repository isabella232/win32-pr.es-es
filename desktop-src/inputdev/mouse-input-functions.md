---
title: 'Funciones de entrada del mouse '
description: .
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47437458cc8ad2bf85ecfa0d8676af8d26c67b89
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797380"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="08bb1-103">Funciones de entrada del mouse </span><span class="sxs-lookup"><span data-stu-id="08bb1-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="08bb1-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="08bb1-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08bb1-105">Tema</span><span class="sxs-lookup"><span data-stu-id="08bb1-105">Topic</span></span></th>
<th><span data-ttu-id="08bb1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="08bb1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08bb1-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-108">Envía mensajes cuando el puntero del mouse sale de una ventana o se mantiene sobre una ventana durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="08bb1-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="08bb1-109">Esta función llama a <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si existe; en caso contrario, lo emula.</span><span class="sxs-lookup"><span data-stu-id="08bb1-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08bb1-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-111">Captura el mouse y realiza un seguimiento de su movimiento hasta que el usuario suelta el botón primario, presiona la tecla ESC o mueve el mouse fuera del rectángulo de arrastre alrededor del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="08bb1-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="08bb1-112">El ancho y el alto del rectángulo de arrastre se especifican mediante los valores <strong>SM_CXDRAG</strong> y <strong>SM_CYDRAG</strong> devueltos por la función <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08bb1-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08bb1-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-114">Recupera un identificador de la ventana (si existe) que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="08bb1-115">Solo una ventana a la vez puede capturar el mouse; esta ventana recibe la entrada del mouse tanto si el cursor está dentro de sus bordes como si no.</span><span class="sxs-lookup"><span data-stu-id="08bb1-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08bb1-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-117">Recupera la hora de doble clic actual del mouse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="08bb1-118">Un doble clic es una serie de dos clics del botón del mouse, el segundo que se produce dentro de un tiempo especificado después de la primera.</span><span class="sxs-lookup"><span data-stu-id="08bb1-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="08bb1-119">La hora de doble clic es el número máximo de milisegundos que pueden producirse entre el primer y el segundo clic de un doble clic.</span><span class="sxs-lookup"><span data-stu-id="08bb1-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="08bb1-120">El tiempo máximo de doble clic es de 5000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="08bb1-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08bb1-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-122">Recupera un historial de hasta 64 coordenadas anteriores del mouse o del lápiz.</span><span class="sxs-lookup"><span data-stu-id="08bb1-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08bb1-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-124">La función <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetiza el movimiento del mouse y los clics de los botones.</span><span class="sxs-lookup"><span data-stu-id="08bb1-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08bb1-125">Esta función se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="08bb1-125">This function has been superseded.</span></span> <span data-ttu-id="08bb1-126">En su lugar, use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08bb1-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08bb1-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-128">Libera la captura del mouse de una ventana en el subproceso actual y restaura el procesamiento normal de la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="08bb1-129">Una ventana que ha capturado el mouse recibe toda la entrada del mouse, independientemente de la posición del cursor, excepto cuando se hace clic en un botón del mouse mientras la zona activa del cursor está en la ventana de otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="08bb1-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08bb1-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-131">Establece la captura del mouse en la ventana especificada que pertenece al subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="08bb1-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08bb1-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-133">Establece la hora de doble clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="08bb1-134">Un doble clic es una serie de dos clics de un botón del mouse, el segundo que se produce dentro de un tiempo especificado después de la primera.</span><span class="sxs-lookup"><span data-stu-id="08bb1-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="08bb1-135">La hora de doble clic es el número máximo de milisegundos que pueden producirse entre el primer y el segundo clic de un doble clic.</span><span class="sxs-lookup"><span data-stu-id="08bb1-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08bb1-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-137">Invierte o restaura el significado de los botones primario y secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08bb1-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="08bb1-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="08bb1-139">Envía mensajes cuando el puntero del mouse sale de una ventana o se mantiene sobre una ventana durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="08bb1-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08bb1-140">La función <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> llama a <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si existe; en caso contrario, <strong>_TrackMouseEvent</strong> emula <strong>TrackMouseEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="08bb1-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

