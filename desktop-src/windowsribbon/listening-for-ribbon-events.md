---
title: Escuchar eventos de la cinta de opciones
description: El marco de la cinta de opciones de Windows usa la infraestructura de seguimiento de eventos para Windows (ETW) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Cinta de Windows, eventos
- Cinta, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359467"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="e8488-105">Escuchar eventos de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="e8488-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="e8488-106">El marco de la cinta de opciones de Windows usa la infraestructura [de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8488-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="e8488-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="e8488-107">Introduction</span></span>

<span data-ttu-id="e8488-108">El mecanismo de eventos de la cinta de opciones está diseñado de forma que el marco informe los eventos de la interfaz de usuario de la cinta de opciones a la aplicación para que pueda supervisar la actividad del usuario, conocer sus patrones de interacción y evaluar las tendencias de uso.</span><span class="sxs-lookup"><span data-stu-id="e8488-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="e8488-109">Esta información se puede usar para refinar la experiencia del usuario para futuras iteraciones de la aplicación de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e8488-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="e8488-110">El uso de los eventos de marco de cinta implica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e8488-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="e8488-111">La aplicación de cinta debe registrar un agente [de escucha de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para recibir notificaciones de eventos de la cinta de opciones desde el marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="e8488-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="e8488-112">El marco de cinta activa las devoluciones de llamada de eventos de la interfaz de usuario en tiempo de ejecución, si la aplicación ha registrado un agente [de escucha de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e8488-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="e8488-113">Eventos admitidos</span><span class="sxs-lookup"><span data-stu-id="e8488-113">Supported events</span></span>

<span data-ttu-id="e8488-114">Los eventos expuestos a las aplicaciones de la cinta de opciones se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8488-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8488-115">Evento</span><span class="sxs-lookup"><span data-stu-id="e8488-115">Event</span></span></th>
<th><span data-ttu-id="e8488-116">Informe de eventos</span><span class="sxs-lookup"><span data-stu-id="e8488-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8488-117">Tabulación activada</span><span class="sxs-lookup"><span data-stu-id="e8488-117">Tab activated</span></span></td>
<td><span data-ttu-id="e8488-118">Identificador de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-118">Command ID</span></span><br/> <span data-ttu-id="e8488-119">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-119">Command name</span></span><br/> <span data-ttu-id="e8488-120">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8488-121">Pestaña contextual activada</span><span class="sxs-lookup"><span data-stu-id="e8488-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="e8488-122">Identificador de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-122">Command ID</span></span><br/> <span data-ttu-id="e8488-123">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-123">Command name</span></span><br/> <span data-ttu-id="e8488-124">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8488-125">Menú de la aplicación abierto</span><span class="sxs-lookup"><span data-stu-id="e8488-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="e8488-126">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8488-127">Menú de aplicación cerrado</span><span class="sxs-lookup"><span data-stu-id="e8488-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="e8488-128">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8488-129">Menú (normal o galería) abierto</span><span class="sxs-lookup"><span data-stu-id="e8488-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="e8488-130">Identificador de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-130">Command ID</span></span><br/> <span data-ttu-id="e8488-131">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-131">Command name</span></span><br/> <span data-ttu-id="e8488-132">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8488-133">Los eventos de menú QAT no se exponen.</span><span class="sxs-lookup"><span data-stu-id="e8488-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8488-134">Menú (normal o galería) cerrado</span><span class="sxs-lookup"><span data-stu-id="e8488-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="e8488-135">Identificador de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-135">Command ID</span></span><br/> <span data-ttu-id="e8488-136">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-136">Command name</span></span><br/> <span data-ttu-id="e8488-137">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8488-138">Los eventos de menú QAT no se exponen.</span><span class="sxs-lookup"><span data-stu-id="e8488-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8488-139">Get-Help</span><span class="sxs-lookup"><span data-stu-id="e8488-139">Command</span></span></td>
<td><span data-ttu-id="e8488-140">Identificador de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-140">Command ID</span></span><br/> <span data-ttu-id="e8488-141">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="e8488-141">Command name</span></span><br/> <span data-ttu-id="e8488-142">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-142">Event verb</span></span><br/> <span data-ttu-id="e8488-143">Una de las siguientes ubicaciones de eventos:</span><span class="sxs-lookup"><span data-stu-id="e8488-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="e8488-144">CABLE</span><span class="sxs-lookup"><span data-stu-id="e8488-144">RIBBON</span></span></li>
<li><span data-ttu-id="e8488-145">QUICKACCESSTOOLBAR</span><span class="sxs-lookup"><span data-stu-id="e8488-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="e8488-146">APPLICATIONMENU</span><span class="sxs-lookup"><span data-stu-id="e8488-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="e8488-147">CONTEXTPOPUP</span><span class="sxs-lookup"><span data-stu-id="e8488-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="e8488-148">IDENTIFICADOR de comando primario</span><span class="sxs-lookup"><span data-stu-id="e8488-148">Parent Command ID</span></span><br/> <span data-ttu-id="e8488-149">Nombre del comando primario</span><span class="sxs-lookup"><span data-stu-id="e8488-149">Parent Command name</span></span><br/> <span data-ttu-id="e8488-150">Uno de los siguientes métodos de invocación:</span><span class="sxs-lookup"><span data-stu-id="e8488-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="e8488-151">HIZO</span><span class="sxs-lookup"><span data-stu-id="e8488-151">CLICK</span></span></li>
<li><span data-ttu-id="e8488-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="e8488-152">KEYTIP</span></span></li>
<li><span data-ttu-id="e8488-153">TECLADO</span><span class="sxs-lookup"><span data-stu-id="e8488-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="e8488-154">ENTRADAS</span><span class="sxs-lookup"><span data-stu-id="e8488-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8488-155">Las galerías de elementos y los cuadros combinados incluyen el índice de elementos seleccionado, pero no incluyen valores de cadena y enteros.</span><span class="sxs-lookup"><span data-stu-id="e8488-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="e8488-156">Los controles de número no incluyen el valor entero.</span><span class="sxs-lookup"><span data-stu-id="e8488-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8488-157">Cinta minimizada</span><span class="sxs-lookup"><span data-stu-id="e8488-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="e8488-158">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8488-159">Cinta expandida (clic en el botón expandir o en anclado)</span><span class="sxs-lookup"><span data-stu-id="e8488-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="e8488-160">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8488-161">Modo de aplicación cambiado</span><span class="sxs-lookup"><span data-stu-id="e8488-161">Application mode switched</span></span></td>
<td><span data-ttu-id="e8488-162">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-162">Event verb</span></span><br/> <span data-ttu-id="e8488-163">IDENTIFICADOR de modo (valor establecido a través de <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="e8488-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8488-164">La aplicación es responsable de desempaquetar este entero para determinar qué modos se establecieron.</span><span class="sxs-lookup"><span data-stu-id="e8488-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8488-165">Información sobre herramientas mostrada</span><span class="sxs-lookup"><span data-stu-id="e8488-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="e8488-166">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="e8488-166">Event verb</span></span><br/> <span data-ttu-id="e8488-167">IDENTIFICADOR de comando primario</span><span class="sxs-lookup"><span data-stu-id="e8488-167">Parent Command ID</span></span><br/> <span data-ttu-id="e8488-168">Nombre del comando primario</span><span class="sxs-lookup"><span data-stu-id="e8488-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e8488-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8488-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8488-170">Guías para desarrolladores del marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="e8488-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="e8488-171">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="e8488-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="e8488-172">Instrucciones para la experiencia del usuario en cinta</span><span class="sxs-lookup"><span data-stu-id="e8488-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="e8488-173">Proceso de diseño de la cinta</span><span class="sxs-lookup"><span data-stu-id="e8488-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

