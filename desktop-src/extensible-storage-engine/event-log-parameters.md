---
description: 'Más información acerca de: parámetros de registro de eventos'
title: Parámetros del registro de eventos
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082833"
---
# <a name="event-log-parameters"></a><span data-ttu-id="4546a-103">Parámetros del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="4546a-103">Event Log Parameters</span></span>


<span data-ttu-id="4546a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4546a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="4546a-105">Parámetros del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="4546a-105">Event Log Parameters</span></span>

<span data-ttu-id="4546a-106">Este tema contiene los parámetros que se usan para el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="4546a-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="4546a-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="4546a-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="4546a-108">Este parámetro controla el tamaño (en bytes) de una caché de mensajes de registro de eventos que contendrá mensajes de registro de eventos emitidos por el motor de base de datos mientras se detiene el servicio EventLog.</span><span class="sxs-lookup"><span data-stu-id="4546a-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="4546a-109">Estos mensajes almacenados en caché se vaciarán en el registro de eventos cuando el servicio esté operativo.</span><span class="sxs-lookup"><span data-stu-id="4546a-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="4546a-110">Se quitarán todos los mensajes que desbordan la caché.</span><span class="sxs-lookup"><span data-stu-id="4546a-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-111">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4546a-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4546a-112">0</span><span class="sxs-lookup"><span data-stu-id="4546a-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4546a-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="4546a-114">Entero</span><span class="sxs-lookup"><span data-stu-id="4546a-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="4546a-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4546a-116">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="4546a-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-117">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="4546a-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4546a-118">Global</span><span class="sxs-lookup"><span data-stu-id="4546a-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-119">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-120">No</span><span class="sxs-lookup"><span data-stu-id="4546a-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-121">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-122">No</span><span class="sxs-lookup"><span data-stu-id="4546a-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-123">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="4546a-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4546a-124">No</span><span class="sxs-lookup"><span data-stu-id="4546a-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-125">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-126">No</span><span class="sxs-lookup"><span data-stu-id="4546a-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-127">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="4546a-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4546a-128">No</span><span class="sxs-lookup"><span data-stu-id="4546a-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-129">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="4546a-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4546a-130">Sí</span><span class="sxs-lookup"><span data-stu-id="4546a-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-131">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-132">All</span><span class="sxs-lookup"><span data-stu-id="4546a-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4546a-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="4546a-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="4546a-134">Este parámetro configura el nivel de detalle de los mensajes de registro de eventos que el motor de base de datos emite para el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="4546a-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="4546a-135">Los números más altos producirán mensajes de registro de eventos más detallados.</span><span class="sxs-lookup"><span data-stu-id="4546a-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-136">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4546a-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4546a-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="4546a-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-138">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4546a-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="4546a-139">Entero</span><span class="sxs-lookup"><span data-stu-id="4546a-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-140">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="4546a-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4546a-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="4546a-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-142">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="4546a-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4546a-143">Instancia</span><span class="sxs-lookup"><span data-stu-id="4546a-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-144">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-145">Sí</span><span class="sxs-lookup"><span data-stu-id="4546a-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-146">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-147">No</span><span class="sxs-lookup"><span data-stu-id="4546a-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-148">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="4546a-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4546a-149">No</span><span class="sxs-lookup"><span data-stu-id="4546a-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-150">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-151">No</span><span class="sxs-lookup"><span data-stu-id="4546a-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-152">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="4546a-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4546a-153">No</span><span class="sxs-lookup"><span data-stu-id="4546a-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-154">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="4546a-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4546a-155">No</span><span class="sxs-lookup"><span data-stu-id="4546a-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-156">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-157">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="4546a-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4546a-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="4546a-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="4546a-159">4</span><span class="sxs-lookup"><span data-stu-id="4546a-159">4</span></span>  

<span data-ttu-id="4546a-160">Este parámetro proporciona una cadena específica de la aplicación que se agregará a los mensajes del registro de eventos emitidos por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4546a-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="4546a-161">Esto permite la correlación sencilla de mensajes de registro de eventos con la aplicación de origen.</span><span class="sxs-lookup"><span data-stu-id="4546a-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="4546a-162">Si se especifica una cadena vacía (como es el valor predeterminado), se utilizará el nombre del archivo ejecutable de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="4546a-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-163">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4546a-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-164">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4546a-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="4546a-165">String</span><span class="sxs-lookup"><span data-stu-id="4546a-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-166">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="4546a-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4546a-167">de 0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="4546a-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-168">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="4546a-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4546a-169">Instancia</span><span class="sxs-lookup"><span data-stu-id="4546a-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-170">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-171">Sí</span><span class="sxs-lookup"><span data-stu-id="4546a-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-172">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-173">No</span><span class="sxs-lookup"><span data-stu-id="4546a-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-174">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="4546a-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4546a-175">No</span><span class="sxs-lookup"><span data-stu-id="4546a-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-176">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-177">No</span><span class="sxs-lookup"><span data-stu-id="4546a-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-178">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="4546a-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4546a-179">No</span><span class="sxs-lookup"><span data-stu-id="4546a-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-180">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="4546a-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4546a-181">No</span><span class="sxs-lookup"><span data-stu-id="4546a-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-182">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-183">All</span><span class="sxs-lookup"><span data-stu-id="4546a-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4546a-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="4546a-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="4546a-185">49</span><span class="sxs-lookup"><span data-stu-id="4546a-185">49</span></span>  

<span data-ttu-id="4546a-186">Este parámetro se puede utilizar para controlar qué registro de eventos utiliza el motor de base de datos para sus mensajes de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="4546a-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="4546a-187">De forma predeterminada, todos los mensajes del registro de eventos Irán al registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4546a-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="4546a-188">Si se configura el nombre de la clave del registro para otro registro de eventos, los mensajes del registro de eventos Irán en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4546a-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-189">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4546a-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-190">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4546a-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="4546a-191">String</span><span class="sxs-lookup"><span data-stu-id="4546a-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-192">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="4546a-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4546a-193">de 0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="4546a-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-194">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="4546a-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4546a-195">Instancia</span><span class="sxs-lookup"><span data-stu-id="4546a-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-196">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-197">Sí</span><span class="sxs-lookup"><span data-stu-id="4546a-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-198">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-199">No</span><span class="sxs-lookup"><span data-stu-id="4546a-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-200">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="4546a-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4546a-201">No</span><span class="sxs-lookup"><span data-stu-id="4546a-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-202">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-203">No</span><span class="sxs-lookup"><span data-stu-id="4546a-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-204">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="4546a-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4546a-205">No</span><span class="sxs-lookup"><span data-stu-id="4546a-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-206">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="4546a-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4546a-207">No</span><span class="sxs-lookup"><span data-stu-id="4546a-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-208">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-209">All</span><span class="sxs-lookup"><span data-stu-id="4546a-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4546a-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="4546a-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="4546a-211">50</span><span class="sxs-lookup"><span data-stu-id="4546a-211">50</span></span>  

<span data-ttu-id="4546a-212">Cuando este parámetro es true, se suprimen los mensajes de registro de eventos informativos que normalmente generará el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4546a-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-213">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4546a-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4546a-214">False</span><span class="sxs-lookup"><span data-stu-id="4546a-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-215">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4546a-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="4546a-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="4546a-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-217">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="4546a-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4546a-218">False, True</span><span class="sxs-lookup"><span data-stu-id="4546a-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-219">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="4546a-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4546a-220">Instancia</span><span class="sxs-lookup"><span data-stu-id="4546a-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-221">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-222">Sí</span><span class="sxs-lookup"><span data-stu-id="4546a-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-223">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="4546a-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4546a-224">No</span><span class="sxs-lookup"><span data-stu-id="4546a-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-225">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="4546a-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4546a-226">No</span><span class="sxs-lookup"><span data-stu-id="4546a-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-227">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-228">No</span><span class="sxs-lookup"><span data-stu-id="4546a-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-229">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="4546a-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4546a-230">No</span><span class="sxs-lookup"><span data-stu-id="4546a-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-231">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="4546a-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4546a-232">No</span><span class="sxs-lookup"><span data-stu-id="4546a-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-233">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="4546a-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4546a-234">All</span><span class="sxs-lookup"><span data-stu-id="4546a-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="4546a-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4546a-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4546a-236"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4546a-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4546a-237">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4546a-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4546a-238"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4546a-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4546a-239">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4546a-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4546a-240"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4546a-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4546a-241">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4546a-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4546a-242">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4546a-242">See Also</span></span>

[<span data-ttu-id="4546a-243">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4546a-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4546a-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="4546a-244">JetInit</span></span>](./jetinit-function.md)
