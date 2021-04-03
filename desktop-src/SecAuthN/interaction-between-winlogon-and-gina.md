---
description: Winlogon y GINA deben comunicar la información de inicialización, controlar la supervisión y notificación de la secuencia de atención segura (SAS) y permitir las actividades de cierre de sesión y cierre.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interacción entre Winlogon y GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083257"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="33f1d-103">Interacción entre Winlogon y GINA </span><span class="sxs-lookup"><span data-stu-id="33f1d-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="33f1d-104">[*Winlogon*](../secgloss/w-gly.md) y [*Gina*](../secgloss/g-gly.md) deben comunicar la información de inicialización, controlar la supervisión y notificación de la [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS) y permitir las actividades de cierre de sesión y cierre.</span><span class="sxs-lookup"><span data-stu-id="33f1d-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="33f1d-105">El estado de Winlogon determina la función GINA a la que se llama para procesar cualquier evento SAS determinado.</span><span class="sxs-lookup"><span data-stu-id="33f1d-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="33f1d-106">Las comunicaciones se producen en el orden que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="33f1d-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="33f1d-107">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33f1d-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33f1d-108">Evento</span><span class="sxs-lookup"><span data-stu-id="33f1d-108">Event</span></span></th>
<th><span data-ttu-id="33f1d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="33f1d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33f1d-110">Arranque de estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="33f1d-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="33f1d-111">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de Gina para notificar a Gina la versión de Winlogon en uso.</span><span class="sxs-lookup"><span data-stu-id="33f1d-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="33f1d-112">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de Gina para proporcionar a Gina las direcciones de las funciones de soporte, un identificador a Winlogon, y para obtener la información de <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> para Gina (que se usará en todas las llamadas futuras a Gina).</span><span class="sxs-lookup"><span data-stu-id="33f1d-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="33f1d-113">Winlogon está en el estado de salida de sesión.</span><span class="sxs-lookup"><span data-stu-id="33f1d-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33f1d-114">No hay una sesión iniciada</span><span class="sxs-lookup"><span data-stu-id="33f1d-114">No one is logged on</span></span></td>
<td><span data-ttu-id="33f1d-115">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-116">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se ha recibido un evento de SAS.</span><span class="sxs-lookup"><span data-stu-id="33f1d-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="33f1d-117">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de Gina, lo que permite que Gina procese la información de autenticación e identificación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="33f1d-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="33f1d-118">Cuando el inicio de sesión se realiza correctamente, Winlogon está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="33f1d-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33f1d-119">El usuario ha iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="33f1d-119">The user is logged on</span></span></td>
<td><span data-ttu-id="33f1d-120">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-121">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se ha recibido un evento de SAS.</span><span class="sxs-lookup"><span data-stu-id="33f1d-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="33f1d-122">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina, lo que permite que Gina presente opciones al usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="33f1d-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33f1d-123">El usuario ha iniciado sesión y desea bloquear el equipo</span><span class="sxs-lookup"><span data-stu-id="33f1d-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="33f1d-124">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-125">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="33f1d-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-126">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-127">GINA devuelve WLX_SAS_ACTION_LOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="33f1d-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="33f1d-128">Winlogon está en el estado de la estación de trabajo bloqueada.</span><span class="sxs-lookup"><span data-stu-id="33f1d-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33f1d-129">El usuario ha iniciado sesión, la estación de trabajo está bloqueada y el usuario desea desbloquear el equipo</span><span class="sxs-lookup"><span data-stu-id="33f1d-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="33f1d-130">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-131">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="33f1d-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-132">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-133">GINA devuelve WLX_SAS_ACTION_UNLOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="33f1d-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33f1d-134">El usuario ha iniciado sesión y el programa llama a la función <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="33f1d-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="33f1d-135">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33f1d-136">El usuario ha iniciado sesión y desea cerrar sesión con SAS</span><span class="sxs-lookup"><span data-stu-id="33f1d-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="33f1d-137">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-138">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="33f1d-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-139">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-140">GINA devuelve WLX_SAS_ACTION_LOGOFF.</span><span class="sxs-lookup"><span data-stu-id="33f1d-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="33f1d-141">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33f1d-142">El usuario ha iniciado sesión y desea cerrar sesión y apagarlo mediante <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="33f1d-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="33f1d-143">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-144">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33f1d-145">El usuario ha iniciado sesión y desea cerrar sesión y cerrarla con SAS</span><span class="sxs-lookup"><span data-stu-id="33f1d-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="33f1d-146">(El GINA supervisa los dispositivos para los eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="33f1d-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="33f1d-147">GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="33f1d-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-148">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-149">GINA devuelve WLX_SAS_ACTION_SHUTDOWN.</span><span class="sxs-lookup"><span data-stu-id="33f1d-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="33f1d-150">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="33f1d-151">Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de Gina.</span><span class="sxs-lookup"><span data-stu-id="33f1d-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
