---
title: Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows
description: Este contenido está destinado a los desarrolladores que desean actualizar las aplicaciones de escritorio para controlar el factor de escala de la pantalla dinámica (también conocido como
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149696"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="fd011-103">Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows</span><span class="sxs-lookup"><span data-stu-id="fd011-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="fd011-104">Este contenido está destinado a los desarrolladores que desean actualizar las aplicaciones de escritorio para controlar los cambios en el factor de escala de la pantalla (puntos por pulgada o PPP) dinámicamente, lo que permite que sus aplicaciones sean nítidas en cualquier pantalla en la que se representen.</span><span class="sxs-lookup"><span data-stu-id="fd011-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="fd011-105">Para empezar, si va a crear una nueva aplicación de Windows desde cero, se recomienda encarecidamente que cree una aplicación [plataforma universal de Windows (UWP)](/windows/uwp/get-started/whats-a-uwp) .</span><span class="sxs-lookup"><span data-stu-id="fd011-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="fd011-106">Las aplicaciones de UWP &mdash; &mdash; se escalan de forma automática y dinámica para cada pantalla en la que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="fd011-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="fd011-107">Las aplicaciones de escritorio que usan tecnologías de programación de Windows anteriores (programación de Win32 sin formato, Windows Forms, Windows Presentation Framework (WPF), etc.) no pueden controlar automáticamente el escalado de PPP sin ningún trabajo de desarrollador adicional.</span><span class="sxs-lookup"><span data-stu-id="fd011-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="fd011-108">Sin este trabajo, las aplicaciones se verán borrosas o con un tamaño incorrecto en muchos escenarios de uso comunes.</span><span class="sxs-lookup"><span data-stu-id="fd011-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="fd011-109">En este documento se proporciona contexto e información sobre lo que implica actualizar una aplicación de escritorio para que se represente correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd011-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="fd011-110">Mostrar factor de escala & PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="fd011-111">A medida que la tecnología de visualización ha progresado, los fabricantes de paneles de pantalla han empaquetado un número cada vez mayor de píxeles en cada unidad de espacio físico en sus paneles.</span><span class="sxs-lookup"><span data-stu-id="fd011-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="fd011-112">Esto ha dado como resultado que los puntos por pulgada (PPP) de los paneles de pantalla modernos sean mucho más altos de lo que históricamente lo han hecho.</span><span class="sxs-lookup"><span data-stu-id="fd011-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="fd011-113">En el pasado, la mayoría de las pantallas tenían 96 píxeles por pulgada lineal de espacio físico (96 PPP). en 2017, se muestra con casi 300 ppp o una versión superior.</span><span class="sxs-lookup"><span data-stu-id="fd011-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="fd011-114">La mayoría de los marcos de interfaz de usuario de escritorio heredados tienen suposiciones integradas que los PPP de la pantalla no cambiarán durante la vigencia del proceso.</span><span class="sxs-lookup"><span data-stu-id="fd011-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="fd011-115">Esta suposición ya no tiene el valor true, con Mostrar PPP que normalmente cambian varias veces a lo largo de la duración de un proceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd011-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="fd011-116">Algunos escenarios comunes en los que los cambios en el factor de escala de presentación/PPP son:</span><span class="sxs-lookup"><span data-stu-id="fd011-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="fd011-117">Configuraciones de varios monitores en las que cada pantalla tiene un factor de escala diferente y la aplicación se mueve de una pantalla a otra (por ejemplo, una pantalla de 4K y 1080p)</span><span class="sxs-lookup"><span data-stu-id="fd011-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="fd011-118">Acoplar y desacoplar un portátil de PPP alto con una pantalla externa de PPP bajo (o viceversa)</span><span class="sxs-lookup"><span data-stu-id="fd011-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="fd011-119">Conexión a través de Escritorio remoto desde un portátil o tableta con un alto PPP a un dispositivo con pocos PPP (o viceversa)</span><span class="sxs-lookup"><span data-stu-id="fd011-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="fd011-120">Cambiar la configuración de un factor de escala de presentación mientras se ejecutan las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fd011-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="fd011-121">En estos casos, las aplicaciones UWP se vuelven a dibujar automáticamente para el nuevo ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="fd011-122">De forma predeterminada, y sin trabajo adicional para desarrolladores, las aplicaciones de escritorio no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="fd011-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="fd011-123">Las aplicaciones de escritorio que no realizan este trabajo adicional para responder a los cambios de PPP pueden aparecer borrosas o con un tamaño incorrecto para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fd011-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="fd011-124">Modo de reconocimiento de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-124">DPI Awareness Mode</span></span>

<span data-ttu-id="fd011-125">Las aplicaciones de escritorio deben indicar a Windows si admiten la escala de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="fd011-126">De forma predeterminada, el sistema considera que los PPP de las aplicaciones de escritorio no reconocen y el mapa de bits ajusta sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="fd011-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="fd011-127">Al establecer uno de los siguientes modos de reconocimiento de PPP disponibles, las aplicaciones pueden indicar explícitamente a Windows cómo desean administrar el escalado de PPP:</span><span class="sxs-lookup"><span data-stu-id="fd011-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="fd011-128">PPP no compatible</span><span class="sxs-lookup"><span data-stu-id="fd011-128">DPI Unaware</span></span>

<span data-ttu-id="fd011-129">Las aplicaciones sin reconocimiento de PPP se representan con un valor de PPP fijo de 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="fd011-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="fd011-130">Cuando estas aplicaciones se ejecutan en una pantalla con una escala de pantalla superior a 96 PPP, Windows extenderá el mapa de bits de la aplicación al tamaño físico esperado.</span><span class="sxs-lookup"><span data-stu-id="fd011-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="fd011-131">Esto hace que la aplicación parezca borrosa.</span><span class="sxs-lookup"><span data-stu-id="fd011-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="fd011-132">Reconocimiento de PPP del sistema</span><span class="sxs-lookup"><span data-stu-id="fd011-132">System DPI Awareness</span></span>

<span data-ttu-id="fd011-133">Las aplicaciones de escritorio que reconocen el sistema PPP normalmente reciben el PPP del monitor conectado principal en el momento del inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="fd011-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="fd011-134">Durante la inicialización, diseñan su interfaz de usuario de forma adecuada (control de tamaño, elección de tamaños de fuente, carga de recursos, etc.) usando ese valor de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd011-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="fd011-135">Por lo tanto, las aplicaciones que tienen en cuenta los PPP del sistema no tienen una escala de PPP (mapa de bits ajustada) por Windows en muestra la representación en ese único ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="fd011-136">Cuando la aplicación se mueve a una pantalla con un factor de escala diferente, o si el factor de escala de la pantalla cambia en otro caso, Windows escalará el mapa de bits de las ventanas de la aplicación, de forma que aparezcan borrosas.</span><span class="sxs-lookup"><span data-stu-id="fd011-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="fd011-137">De hecho, las aplicaciones de escritorio con reconocimiento de PPP del sistema solo se representan de forma nítida en un solo factor de escala de pantalla, lo que se vuelve borrosa cada vez que cambia el PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="fd011-138">Reconocimiento de PPP de Per-Monitor y Per-Monitor (V2)</span><span class="sxs-lookup"><span data-stu-id="fd011-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="fd011-139">Se recomienda que las aplicaciones de escritorio se actualicen para usar el modo de reconocimiento de PPP por monitor, lo que permite que se representen de inmediato siempre que cambie el PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="fd011-140">Cuando una aplicación notifica a Windows que desea ejecutar en este modo, Windows no creará un mapa de bits de la aplicación cuando cambie el PPP, sino que enviará [WM \_ DPICHANGED](wm-dpichanged.md) a la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd011-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="fd011-141">Después, es responsabilidad completa de la aplicación controlar el cambio de tamaño para el nuevo ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="fd011-142">La mayoría de los marcos de interfaz de usuario que usan las aplicaciones de escritorio (controles comunes de Windows (comctl32), Windows Forms, Windows Presentation Framework, etc.) no admiten el escalado de PPP automático, lo que obliga a los desarrolladores a cambiar el tamaño y la posición del contenido de sus propias ventanas.</span><span class="sxs-lookup"><span data-stu-id="fd011-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="fd011-143">Hay dos versiones de Per-Monitor reconocimiento de que una aplicación puede registrarse como: versión 1 y versión 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="fd011-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="fd011-144">El registro de un proceso como en ejecución en el modo de reconocimiento de PMv2 produce:</span><span class="sxs-lookup"><span data-stu-id="fd011-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="fd011-145">La aplicación a la que se notifica cuando cambia el PPP (el HWND de nivel superior y el secundario)</span><span class="sxs-lookup"><span data-stu-id="fd011-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="fd011-146">La aplicación ve los píxeles sin formato de cada pantalla</span><span class="sxs-lookup"><span data-stu-id="fd011-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="fd011-147">La aplicación nunca está escalada como mapa de bits de Windows</span><span class="sxs-lookup"><span data-stu-id="fd011-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="fd011-148">Área no cliente automática (título de ventana, barras de desplazamiento, etc.) Ajuste de escala de PPP por Windows</span><span class="sxs-lookup"><span data-stu-id="fd011-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="fd011-149">Cuadros de diálogo Win32 (desde [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) ajuste automático de PPP por Windows</span><span class="sxs-lookup"><span data-stu-id="fd011-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="fd011-150">Los recursos de mapa de bits dibujados por temas en controles comunes (casillas, el fondo de los botones, etc.) se representan automáticamente en el factor de escala de PPP adecuado.</span><span class="sxs-lookup"><span data-stu-id="fd011-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="fd011-151">Cuando se ejecuta en el modo de reconocimiento de Per-Monitor V2, se notifica a las aplicaciones cuando cambia su ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="fd011-152">Si una aplicación no cambia de tamaño para el nuevo valor de PPP, la interfaz de usuario de la aplicación aparecerá demasiado pequeña o demasiado grande (dependiendo de la diferencia en los valores de PPP anterior y nuevo).</span><span class="sxs-lookup"><span data-stu-id="fd011-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="fd011-153">El reconocimiento de Per-Monitor V1 (PMv1) es muy limitado.</span><span class="sxs-lookup"><span data-stu-id="fd011-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="fd011-154">Se recomienda que las aplicaciones usen PMv2.</span><span class="sxs-lookup"><span data-stu-id="fd011-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="fd011-155">En la tabla siguiente se muestra cómo se representarán las aplicaciones en distintos escenarios:</span><span class="sxs-lookup"><span data-stu-id="fd011-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd011-156">Modo de reconocimiento de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="fd011-157">Versión de Windows introducida</span><span class="sxs-lookup"><span data-stu-id="fd011-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="fd011-158">Vista de PPP de la aplicación</span><span class="sxs-lookup"><span data-stu-id="fd011-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="fd011-159">Comportamiento en cambio de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd011-160">Consciente</span><span class="sxs-lookup"><span data-stu-id="fd011-160">Unaware</span></span></td>
<td><span data-ttu-id="fd011-161">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-161">N/A</span></span></td>
<td><span data-ttu-id="fd011-162">Todas las pantallas tienen 96 PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="fd011-163">Expansión de mapas de bits (borrosa)</span><span class="sxs-lookup"><span data-stu-id="fd011-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd011-164">System</span><span class="sxs-lookup"><span data-stu-id="fd011-164">System</span></span></td>
<td><span data-ttu-id="fd011-165">Vista</span><span class="sxs-lookup"><span data-stu-id="fd011-165">Vista</span></span></td>
<td><span data-ttu-id="fd011-166">Todas las pantallas tienen el mismo PPP (el PPP de la pantalla principal en el momento en que se inició la sesión de usuario actual)</span><span class="sxs-lookup"><span data-stu-id="fd011-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="fd011-167">Expansión de mapas de bits (borrosa)</span><span class="sxs-lookup"><span data-stu-id="fd011-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd011-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="fd011-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="fd011-169">8.1</span><span class="sxs-lookup"><span data-stu-id="fd011-169">8.1</span></span></td>
<td><span data-ttu-id="fd011-170">El PPP de la pantalla en la que se encuentra principalmente la ventana de la aplicación</span><span class="sxs-lookup"><span data-stu-id="fd011-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="fd011-171">El HWND de nivel superior recibe una notificación de cambio de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="fd011-172">Sin escala de PPP de ningún elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fd011-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd011-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="fd011-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="fd011-174">Windows 10 Creators Update (1703)</span><span class="sxs-lookup"><span data-stu-id="fd011-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="fd011-175">El PPP de la pantalla en la que se encuentra principalmente la ventana de la aplicación</span><span class="sxs-lookup"><span data-stu-id="fd011-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="fd011-176">Los HWND de nivel superior <span class="underline">y</span> secundarios reciben una notificación de cambio de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="fd011-177"><span class="underline">Escala de PPP automática de:</span>
</span><span class="sxs-lookup"><span data-stu-id="fd011-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="fd011-178">Área no cliente</span><span class="sxs-lookup"><span data-stu-id="fd011-178">Non-client area</span></span></li>
<li><span data-ttu-id="fd011-179">Mapas de bits dibujados por temas en controles comunes (comctl32 V6)</span><span class="sxs-lookup"><span data-stu-id="fd011-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="fd011-180">Cuadros de diálogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span><span class="sxs-lookup"><span data-stu-id="fd011-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="fd011-181">Reconocimiento de PPP por monitor (V1)</span><span class="sxs-lookup"><span data-stu-id="fd011-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="fd011-182">Per-Monitor el modo de reconocimiento de PPP (PMv1) V1 se presentó con Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="fd011-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="fd011-183">Este modo de reconocimiento de PPP es muy limitado y solo ofrece la funcionalidad que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="fd011-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="fd011-184">Se recomienda que las aplicaciones de escritorio usen el modo de reconocimiento de Per-Monitor V2, compatible con Windows 10 1703 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fd011-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="fd011-185">La compatibilidad inicial para el reconocimiento por monitor solo ofrecía las aplicaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd011-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="fd011-186">Los HWND de nivel superior reciben una notificación de un cambio de PPP y proporcionan un nuevo tamaño sugerido</span><span class="sxs-lookup"><span data-stu-id="fd011-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="fd011-187">Windows no ajustará el mapa de bits de la interfaz de usuario de la aplicación</span><span class="sxs-lookup"><span data-stu-id="fd011-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="fd011-188">La aplicación ve todas las pantallas en píxeles físicos (consulte virtualización)</span><span class="sxs-lookup"><span data-stu-id="fd011-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="fd011-189">En Windows 10 1607 o posterior, las aplicaciones de PMv1 también pueden llamar a [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM \_ NCCREATE para solicitar que Windows escale correctamente el área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fd011-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="fd011-190">Compatibilidad con el ajuste de escala de PPP por monitor mediante la tecnología/marco de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fd011-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="fd011-191">En la tabla siguiente se muestra el nivel de compatibilidad con el reconocimiento de PPP por monitor ofrecido por diversos marcos de interfaz de usuario de Windows a partir de Windows 10 1703:</span><span class="sxs-lookup"><span data-stu-id="fd011-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd011-192">Plataforma/tecnología</span><span class="sxs-lookup"><span data-stu-id="fd011-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="fd011-193">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="fd011-193">Support</span></span></th>
<th><span data-ttu-id="fd011-194">Versión del SO.</span><span class="sxs-lookup"><span data-stu-id="fd011-194">OS Version</span></span></th>
<th><span data-ttu-id="fd011-195">Ajuste de escala de PPP controlado por</span><span class="sxs-lookup"><span data-stu-id="fd011-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="fd011-196">Lecturas adicionales</span><span class="sxs-lookup"><span data-stu-id="fd011-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd011-197">Plataforma universal de Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="fd011-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="fd011-198">Completo</span><span class="sxs-lookup"><span data-stu-id="fd011-198">Full</span></span></td>
<td><span data-ttu-id="fd011-199">1607</span><span class="sxs-lookup"><span data-stu-id="fd011-199">1607</span></span></td>
<td><span data-ttu-id="fd011-200">Marco de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fd011-200">UI framework</span></span></td>
<td><span data-ttu-id="fd011-201"><a href="/windows/uwp/get-started/whats-a-uwp">Plataforma universal de Windows (UWP)</a></span><span class="sxs-lookup"><span data-stu-id="fd011-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd011-202">Win32/controles comunes sin formato V6 (comctl32.dll)</span><span class="sxs-lookup"><span data-stu-id="fd011-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="fd011-203">Mensajes de notificación de cambio de PPP enviados a todos los HWND</span><span class="sxs-lookup"><span data-stu-id="fd011-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="fd011-204">Los activos dibujados por temas se representan correctamente en controles comunes</span><span class="sxs-lookup"><span data-stu-id="fd011-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="fd011-205">Escala de PPP automática para cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="fd011-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="fd011-206">1703</span><span class="sxs-lookup"><span data-stu-id="fd011-206">1703</span></span></td>
<td><span data-ttu-id="fd011-207">Application</span><span class="sxs-lookup"><span data-stu-id="fd011-207">Application</span></span></td>
<td><span data-ttu-id="fd011-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Ejemplo de GitHub</a></span><span class="sxs-lookup"><span data-stu-id="fd011-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd011-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fd011-209">Windows Forms</span></span></td>
<td><span data-ttu-id="fd011-210">Escala de PPP por monitor automática limitada para algunos controles</span><span class="sxs-lookup"><span data-stu-id="fd011-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="fd011-211">1703</span><span class="sxs-lookup"><span data-stu-id="fd011-211">1703</span></span></td>
<td><span data-ttu-id="fd011-212">Marco de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fd011-212">UI framework</span></span></td>
<td><span data-ttu-id="fd011-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Compatibilidad con PPP alta en Windows Forms</a></span><span class="sxs-lookup"><span data-stu-id="fd011-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd011-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="fd011-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="fd011-215">Las aplicaciones WPF nativas escalarán PPP de WPF hospedadas en otros marcos y otros marcos de trabajo hospedados en WPF no se escalan automáticamente</span><span class="sxs-lookup"><span data-stu-id="fd011-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="fd011-216">1607</span><span class="sxs-lookup"><span data-stu-id="fd011-216">1607</span></span></td>
<td><span data-ttu-id="fd011-217">Marco de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fd011-217">UI framework</span></span></td>
<td><span data-ttu-id="fd011-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Ejemplo de GitHub</a></span><span class="sxs-lookup"><span data-stu-id="fd011-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd011-219">GDI</span><span class="sxs-lookup"><span data-stu-id="fd011-219">GDI</span></span></td>
<td><span data-ttu-id="fd011-220">None</span><span class="sxs-lookup"><span data-stu-id="fd011-220">None</span></span></td>
<td><span data-ttu-id="fd011-221">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-221">N/A</span></span></td>
<td><span data-ttu-id="fd011-222">Application</span><span class="sxs-lookup"><span data-stu-id="fd011-222">Application</span></span></td>
<td><span data-ttu-id="fd011-223">Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">escala de PPP alta-PPP</a></span><span class="sxs-lookup"><span data-stu-id="fd011-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd011-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="fd011-224">GDI+</span></span></td>
<td><span data-ttu-id="fd011-225">None</span><span class="sxs-lookup"><span data-stu-id="fd011-225">None</span></span></td>
<td><span data-ttu-id="fd011-226">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-226">N/A</span></span></td>
<td><span data-ttu-id="fd011-227">Application</span><span class="sxs-lookup"><span data-stu-id="fd011-227">Application</span></span></td>
<td><span data-ttu-id="fd011-228">Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">escala de PPP alta-PPP</a></span><span class="sxs-lookup"><span data-stu-id="fd011-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd011-229">MFC</span><span class="sxs-lookup"><span data-stu-id="fd011-229">MFC</span></span></td>
<td><span data-ttu-id="fd011-230">None</span><span class="sxs-lookup"><span data-stu-id="fd011-230">None</span></span></td>
<td><span data-ttu-id="fd011-231">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-231">N/A</span></span></td>
<td><span data-ttu-id="fd011-232">Application</span><span class="sxs-lookup"><span data-stu-id="fd011-232">Application</span></span></td>
<td><span data-ttu-id="fd011-233">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="fd011-234">Actualizar aplicaciones existentes</span><span class="sxs-lookup"><span data-stu-id="fd011-234">Updating Existing Applications</span></span>

<span data-ttu-id="fd011-235">Para actualizar una aplicación de escritorio existente para controlar el escalado de PPP correctamente, debe actualizarse de forma que, como mínimo, las partes importantes de su interfaz de usuario se actualicen para responder a los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="fd011-236">La mayoría de las aplicaciones de escritorio se ejecutan en modo de reconocimiento de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd011-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="fd011-237">Las aplicaciones con reconocimiento de PPP del sistema normalmente se escalan al ppp de la pantalla principal (la pantalla en la que se encontraba la bandeja del sistema en el momento en que se inició la sesión de Windows).</span><span class="sxs-lookup"><span data-stu-id="fd011-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="fd011-238">Cuando cambia el PPP, Windows ajustará el mapa de bits de la interfaz de usuario de estas aplicaciones, lo que a menudo resulta que son borrosos.</span><span class="sxs-lookup"><span data-stu-id="fd011-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="fd011-239">Al actualizar una aplicación compatible con PPP del sistema a reconocimiento de PPP por monitor, el código que controla el diseño de la interfaz de usuario debe actualizarse de forma que se realice no solo durante la inicialización de la aplicación, sino que también siempre que se reciba una notificación de cambio de PPP ([WM \_ DPICHANGED](wm-dpichanged.md) en el caso de Win32).</span><span class="sxs-lookup"><span data-stu-id="fd011-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="fd011-240">Normalmente, esto implica volver a visitar cualquier suposición en el código que la interfaz de usuario solo debe escalar una vez.</span><span class="sxs-lookup"><span data-stu-id="fd011-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="fd011-241">Además, en el caso de la programación de Win32, muchas API de Win32 no tienen ningún contexto de pantalla o PPP, por lo que solo devolverán valores relativos al valor de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd011-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="fd011-242">Puede ser útil para grep a través del código con el fin de buscar algunas de estas API y reemplazarlas por variantes con reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="fd011-243">Algunas de las API comunes que tienen variantes con reconocimiento de PPP son:</span><span class="sxs-lookup"><span data-stu-id="fd011-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="fd011-244">Versión de PPP única</span><span class="sxs-lookup"><span data-stu-id="fd011-244">Single DPI version</span></span>   | <span data-ttu-id="fd011-245">Versión de Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="fd011-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="fd011-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="fd011-246">GetSystemMetrics</span></span>     | <span data-ttu-id="fd011-247">GetSystemMetricsForDpi</span><span class="sxs-lookup"><span data-stu-id="fd011-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="fd011-248">AdjustWindowRectEx</span><span class="sxs-lookup"><span data-stu-id="fd011-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="fd011-249">AdjustWindowRectExForDpi</span><span class="sxs-lookup"><span data-stu-id="fd011-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="fd011-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="fd011-250">SystemParametersInfo</span></span> | <span data-ttu-id="fd011-251">SystemParametersInfoForDpi</span><span class="sxs-lookup"><span data-stu-id="fd011-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="fd011-252">GetDpiForMonitor</span><span class="sxs-lookup"><span data-stu-id="fd011-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="fd011-253">GetDpiForWindow</span><span class="sxs-lookup"><span data-stu-id="fd011-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="fd011-254">También es una buena idea buscar los tamaños codificados de forma rígida en el código base que suponen un PPP constante y los reemplazan por código que cuenta correctamente para la escala de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="fd011-255">A continuación se muestra un ejemplo que incorpora todas estas sugerencias:</span><span class="sxs-lookup"><span data-stu-id="fd011-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="fd011-256">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fd011-256">Example:</span></span>

<span data-ttu-id="fd011-257">En el ejemplo siguiente se muestra un caso de Win32 simplificado de creación de un HWND secundario.</span><span class="sxs-lookup"><span data-stu-id="fd011-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="fd011-258">La llamada a CreateWindow supone que la aplicación se está ejecutando a 96 PPP y que el tamaño y la posición del botón serán correctos en PPP superior:</span><span class="sxs-lookup"><span data-stu-id="fd011-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="fd011-259">El código actualizado siguiente muestra:</span><span class="sxs-lookup"><span data-stu-id="fd011-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="fd011-260">El código de creación de ventanas PPP escala la posición y el tamaño del HWND secundario para el PPP de su ventana primaria</span><span class="sxs-lookup"><span data-stu-id="fd011-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="fd011-261">Responder al cambio de PPP cambiando la posición y el tamaño del HWND secundario</span><span class="sxs-lookup"><span data-stu-id="fd011-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="fd011-262">Los tamaños codificados de forma rígida se quitan y reemplazan por código que responde a los cambios de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="fd011-263">Al actualizar una aplicación compatible con PPP del sistema, algunos de los pasos que debe seguir son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd011-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="fd011-264">Marque el proceso como reconocimiento de PPP por monitor (V2) mediante un manifiesto de aplicación (u otro método, en función de los marcos de interfaz de usuario utilizados).</span><span class="sxs-lookup"><span data-stu-id="fd011-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="fd011-265">Haga que la lógica de diseño de la interfaz de usuario sea reutilizable y muévala del código de inicialización de la aplicación para que se pueda reutilizar cuando se produzca un cambio de PPP (WM \_ DPICHANGED en el caso de la programación de Windows (Win32)).</span><span class="sxs-lookup"><span data-stu-id="fd011-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="fd011-266">Invalide cualquier código que asuma que no es necesario actualizar nunca la información sensible a los PPP (PPP, fuentes, tamaños, etc.).</span><span class="sxs-lookup"><span data-stu-id="fd011-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="fd011-267">Es una práctica muy común almacenar en caché los tamaños de fuente y los valores de PPP en la inicialización del proceso.</span><span class="sxs-lookup"><span data-stu-id="fd011-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="fd011-268">Al actualizar una aplicación para que sea compatible con PPP por monitor, se deben volver a evaluar los datos con distinción de PPP cada vez que se encuentre un nuevo ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="fd011-269">Cuando se produce un cambio de PPP, vuelva a cargar (o vuelva a rasterizar) los recursos de mapa de bits para el nuevo PPP o, opcionalmente, ajuste el mapa de bits a los activos cargados actualmente en el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="fd011-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="fd011-270">Grep para las API que no son compatibles con PPP Per-Monitor y las reemplazan por Per-Monitor API que reconocen los PPP (si procede).</span><span class="sxs-lookup"><span data-stu-id="fd011-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="fd011-271">Ejemplo: Reemplace GetSystemMetrics por GetSystemMetricsForDpi.</span><span class="sxs-lookup"><span data-stu-id="fd011-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="fd011-272">Pruebe la aplicación en un sistema de varios PPP o múltiples pantallas.</span><span class="sxs-lookup"><span data-stu-id="fd011-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="fd011-273">En el caso de las ventanas de nivel superior de la aplicación que no se puedan actualizar a una escala de PPP adecuada, use el escalado de PPP en modo mixto (que se describe a continuación) para permitir que el sistema ajuste los mapas de bits de estas ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="fd011-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="fd011-274">Ajuste de escala de PPP Mixed-Mode (escala de PPP de subproceso)</span><span class="sxs-lookup"><span data-stu-id="fd011-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="fd011-275">Al actualizar una aplicación para admitir el reconocimiento de PPP por monitor, a veces puede resultar poco práctico o imposible actualizar cada ventana de la aplicación en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="fd011-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="fd011-276">Esto puede ser simplemente debido al tiempo y al esfuerzo necesarios para actualizar y probar todas las interfaces de usuario, o porque no posee todo el código de interfaz de usuario que necesita ejecutar (si la aplicación puede cargar una interfaz de usuario de terceros).</span><span class="sxs-lookup"><span data-stu-id="fd011-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="fd011-277">En estas situaciones, Windows ofrece una manera de facilitar el mundo del reconocimiento por monitor, ya que permite ejecutar algunas de las ventanas de la aplicación (solo de nivel superior) en su modo de reconocimiento de PPP original mientras se centra el tiempo y la actualización de energía de las partes más importantes de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fd011-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="fd011-278">A continuación se muestra una ilustración del aspecto que podría tener: actualice la interfaz de usuario de la aplicación principal ("ventana principal" en la ilustración) para ejecutar con reconocimiento de PPP por monitor mientras ejecuta otras ventanas en su modo existente ("ventana secundaria").</span><span class="sxs-lookup"><span data-stu-id="fd011-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![diferencias en el escalado de PPP entre los modos de reconocimiento](images/hub-page-illustrations.png)

<span data-ttu-id="fd011-280">Antes de la actualización de aniversario de Windows 10 (1607), el modo de reconocimiento de PPP de un proceso era una propiedad de todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="fd011-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="fd011-281">A partir de la actualización de aniversario de Windows 10, esta propiedad se puede establecer ahora por ventana **de nivel superior** .</span><span class="sxs-lookup"><span data-stu-id="fd011-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="fd011-282">(Las ventanas **secundarias** deben seguir coincidiendo con el tamaño de escala de su elemento primario). Una ventana de nivel superior se define como una ventana sin elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fd011-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="fd011-283">Normalmente, se trata de una ventana "normal" con botones minimizar, maximizar y cerrar.</span><span class="sxs-lookup"><span data-stu-id="fd011-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="fd011-284">El escenario para el que está diseñado el reconocimiento de PPP de subprocesos es tener una interfaz de usuario secundaria escalada por Windows (mapa de bits ampliado) mientras se centra el tiempo y los recursos en la actualización de la interfaz de usuario principal.</span><span class="sxs-lookup"><span data-stu-id="fd011-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="fd011-285">Para habilitar el reconocimiento de PPP de subprocesos, llame a [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes y después de cualquier llamada de creación de ventana.</span><span class="sxs-lookup"><span data-stu-id="fd011-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="fd011-286">La ventana que se crea se asociará con el reconocimiento de PPP que establezca a través de SetThreadDpiAwarenessContext.</span><span class="sxs-lookup"><span data-stu-id="fd011-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="fd011-287">Use la segunda llamada para restaurar el reconocimiento actual del subproceso s ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="fd011-288">Aunque el escalado de PPP de subproceso permite confiar en Windows para que realice parte de la escala de PPP de la aplicación, puede aumentar la complejidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd011-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="fd011-289">Es importante que comprenda las desventajas de este enfoque y la naturaleza de las complejidades que presenta.</span><span class="sxs-lookup"><span data-stu-id="fd011-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="fd011-290">Para obtener más información sobre el reconocimiento de PPP de subprocesos, vea el tema sobre [la escala de PPP en modo mixto y las API que reconocen ppp.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="fd011-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="fd011-291">Probar los cambios</span><span class="sxs-lookup"><span data-stu-id="fd011-291">Testing Your Changes</span></span>

<span data-ttu-id="fd011-292">Después de haber actualizado la aplicación para que sea compatible con los ppp por monitor, es importante validar que la aplicación responde correctamente a los cambios de PPP en un entorno de PPP mixto.</span><span class="sxs-lookup"><span data-stu-id="fd011-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="fd011-293">Algunos detalles de la prueba incluyen:</span><span class="sxs-lookup"><span data-stu-id="fd011-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="fd011-294">Mover ventanas de aplicaciones hacia delante y hacia atrás entre pantallas de distintos valores de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="fd011-295">Inicio de la aplicación en presentaciones de distintos valores de PPP</span><span class="sxs-lookup"><span data-stu-id="fd011-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="fd011-296">Cambiar el factor de escala para el monitor mientras la aplicación se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="fd011-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="fd011-297">Cambiar la presentación que se usa como pantalla principal, _cerrar la sesión de Windows_ y volver a probar la aplicación después de volver a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fd011-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="fd011-298">Esto es especialmente útil para buscar código que usa dimensiones o tamaños codificados de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="fd011-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="fd011-299">Errores comunes (Win32)</span><span class="sxs-lookup"><span data-stu-id="fd011-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="fd011-300">**No usar el rectángulo sugerido proporcionado en WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="fd011-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="fd011-301">Cuando Windows envía un mensaje de [**WM \_ DPICHANGED**](wm-dpichanged.md) a la ventana de la aplicación, este mensaje incluye un rectángulo sugerido que debe usar para cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fd011-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="fd011-302">Es fundamental que la aplicación use este rectángulo para cambiar el tamaño, ya que esto hará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fd011-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="fd011-303">Asegúrese de que el cursor del mouse permanecerá en la misma posición relativa en la ventana al arrastrar entre las pantallas.</span><span class="sxs-lookup"><span data-stu-id="fd011-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="fd011-304">Impedir que la ventana de la aplicación entre en un ciclo recursivo de cambio de PPP en el que un cambio de PPP desencadena un cambio de PPP posterior, que desencadena otro cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="fd011-305">Si tiene requisitos específicos de la aplicación que impiden usar el rectángulo sugerido que Windows proporciona en el mensaje de DPICHANGED de WM \_ , consulte [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="fd011-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="fd011-306">Este mensaje se puede usar para dar a Windows un tamaño deseado que le gustaría usar una vez que se ha producido el cambio de PPP, sin dejar de seguir los problemas descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fd011-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="fd011-307">**Falta de documentación sobre la virtualización**</span><span class="sxs-lookup"><span data-stu-id="fd011-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="fd011-308">Cuando un HWND o un proceso se está ejecutando como PPP no compatible o con PPP del sistema, puede ser un mapa de bits ajustado por Windows.</span><span class="sxs-lookup"><span data-stu-id="fd011-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="fd011-309">Cuando esto sucede, Windows escala y convierte la información sensible a los PPP de algunas API en el espacio de coordenadas del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="fd011-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="fd011-310">Por ejemplo, si un subproceso sin reconocimiento de PPP consulta el tamaño de la pantalla mientras se ejecuta en una pantalla de PPP alta, Windows virtualizará la respuesta proporcionada a la aplicación como si estuviera en unidades de 96 ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="fd011-311">Como alternativa, cuando un subproceso de reconocimiento de PPP del sistema está interactuando con una pantalla en un PPP diferente del que estaba en uso al iniciar la sesión del usuario actual, Windows redimensiona algunas llamadas de API en el espacio de coordenadas que usaría HWND si se estaba ejecutando en su factor de escala de PPP original.</span><span class="sxs-lookup"><span data-stu-id="fd011-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="fd011-312">Al actualizar la aplicación de escritorio a la escala de PPP correctamente, puede resultar difícil saber qué llamadas de API pueden devolver valores virtualizados según el contexto del subproceso. Esta información no está suficientemente documentada por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fd011-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="fd011-313">Tenga en cuenta que si llama a cualquier API del sistema a partir de un contexto de subproceso que no sea compatible con el sistema o con PPP, el valor devuelto podría estar virtualizado.</span><span class="sxs-lookup"><span data-stu-id="fd011-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="fd011-314">Como tal, asegúrese de que el subproceso se está ejecutando en el contexto de PPP que espera al interactuar con la pantalla o las ventanas individuales.</span><span class="sxs-lookup"><span data-stu-id="fd011-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="fd011-315">Al cambiar temporalmente el contexto de PPP de un subproceso mediante [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), asegúrese de restaurar el contexto anterior cuando haya terminado de evitar que se produzca un comportamiento incorrecto en otra parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd011-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="fd011-316">**Muchas API de Windows no tienen un contexto de PPP**</span><span class="sxs-lookup"><span data-stu-id="fd011-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="fd011-317">Muchas API heredadas de Windows no incluyen un contexto de PPP o HWND como parte de su interfaz.</span><span class="sxs-lookup"><span data-stu-id="fd011-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="fd011-318">Como resultado, los desarrolladores suelen tener que realizar trabajo adicional para controlar el escalado de cualquier información sensible a los PPP, como tamaños, puntos o iconos.</span><span class="sxs-lookup"><span data-stu-id="fd011-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="fd011-319">Por ejemplo, los desarrolladores que usan [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) deben tener en el mapa de bits los iconos de stretch cargados o usar API alternativas para cargar los iconos de tamaño correcto para el PPP adecuado, como [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span><span class="sxs-lookup"><span data-stu-id="fd011-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="fd011-320">**Restablecimiento forzado de reconocimiento de PPP en todo el proceso**</span><span class="sxs-lookup"><span data-stu-id="fd011-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="fd011-321">En general, el modo de reconocimiento de PPP del proceso no se puede cambiar después de la inicialización del proceso.</span><span class="sxs-lookup"><span data-stu-id="fd011-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="fd011-322">Sin embargo, Windows puede cambiar forzosamente el modo de reconocimiento de PPP del proceso si intenta romper el requisito de que todos los HWND de un árbol de ventana tienen el mismo modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="fd011-323">En todas las versiones de Windows, a partir de Windows 10 1703, no es posible tener diferentes HWND en un árbol HWND que se ejecuten en distintos modos de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="fd011-324">Si intenta crear una relación de elementos primarios y secundarios que interrumpa esta regla, se puede restablecer el reconocimiento de PPP de todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="fd011-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="fd011-325">Esto se puede activar mediante:</span><span class="sxs-lookup"><span data-stu-id="fd011-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="fd011-326">Una llamada a CreateWindow en la que la ventana primaria pasada tiene un modo de reconocimiento de PPP diferente que el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="fd011-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="fd011-327">Una llamada a SetParent en la que las dos ventanas están asociadas a distintos modos de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd011-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="fd011-328">En la tabla siguiente se muestra lo que ocurre si intenta infringir esta regla:</span><span class="sxs-lookup"><span data-stu-id="fd011-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="fd011-329">Operación</span><span class="sxs-lookup"><span data-stu-id="fd011-329">Operation</span></span>                 | <span data-ttu-id="fd011-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd011-330">Windows 8.1</span></span>                                  | <span data-ttu-id="fd011-331">Windows 10 (1607 y versiones anteriores)</span><span class="sxs-lookup"><span data-stu-id="fd011-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="fd011-332">Windows 10 (1703 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="fd011-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="fd011-333">CreateWindow (en proceso)</span><span class="sxs-lookup"><span data-stu-id="fd011-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="fd011-334">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-334">N/A</span></span>                                          | <span data-ttu-id="fd011-335">Los **elementos secundarios heredan** (modo mixto)</span><span class="sxs-lookup"><span data-stu-id="fd011-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="fd011-336">Los **elementos secundarios heredan** (modo mixto)</span><span class="sxs-lookup"><span data-stu-id="fd011-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="fd011-337">CreateWindow (Cross-proc)</span><span class="sxs-lookup"><span data-stu-id="fd011-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="fd011-338">**Restablecimiento forzado** (del proceso del llamador)</span><span class="sxs-lookup"><span data-stu-id="fd011-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="fd011-339">Los **elementos secundarios heredan** (modo mixto)</span><span class="sxs-lookup"><span data-stu-id="fd011-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="fd011-340">**Restablecimiento forzado** (del proceso del llamador)</span><span class="sxs-lookup"><span data-stu-id="fd011-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="fd011-341">SetParent (en proceso)</span><span class="sxs-lookup"><span data-stu-id="fd011-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="fd011-342">N/D</span><span class="sxs-lookup"><span data-stu-id="fd011-342">N/A</span></span>                                          | <span data-ttu-id="fd011-343">**Restablecimiento forzado** (del proceso actual)</span><span class="sxs-lookup"><span data-stu-id="fd011-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="fd011-344">**Error (error** de \_ Estado no válido \_ )</span><span class="sxs-lookup"><span data-stu-id="fd011-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="fd011-345">SetParent (entre procedimientos)</span><span class="sxs-lookup"><span data-stu-id="fd011-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="fd011-346">**Restablecimiento forzado** (del proceso de la ventana secundaria)</span><span class="sxs-lookup"><span data-stu-id="fd011-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="fd011-347">**Restablecimiento forzado** (del proceso de la ventana secundaria)</span><span class="sxs-lookup"><span data-stu-id="fd011-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="fd011-348">**Restablecimiento forzado** (del proceso de la ventana secundaria)</span><span class="sxs-lookup"><span data-stu-id="fd011-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fd011-349">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd011-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd011-350">Referencia de la API de PPP alta</span><span class="sxs-lookup"><span data-stu-id="fd011-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="fd011-351">Escala de PPP en modo mixto y API que reconocen ppp.</span><span class="sxs-lookup"><span data-stu-id="fd011-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

