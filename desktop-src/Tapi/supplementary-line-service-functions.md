---
description: Las funciones de servicio de línea suplementaria se enumeran por Categoría en los temas siguientes.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funciones de servicio de línea complementarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687496"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="8c5b2-103">Funciones de servicio de línea complementarias</span><span class="sxs-lookup"><span data-stu-id="8c5b2-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="8c5b2-104">Las funciones de servicio de línea suplementaria se enumeran por Categoría en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="8c5b2-105">Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje de respuesta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="8c5b2-106">Si la función devuelve siempre su resultado a la aplicación inmediatamente, la función se considera [*sincrónica*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8c5b2-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="8c5b2-107">A continuación se muestra una agrupación funcional de las funciones de servicio de línea complementarias:</span><span class="sxs-lookup"><span data-stu-id="8c5b2-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="8c5b2-108">Agentes</span><span class="sxs-lookup"><span data-stu-id="8c5b2-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="8c5b2-109">Prioridad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8c5b2-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="8c5b2-110">Modo y velocidad del portador</span><span class="sxs-lookup"><span data-stu-id="8c5b2-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="8c5b2-111">Llamar a Accept y Redirect</span><span class="sxs-lookup"><span data-stu-id="8c5b2-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="8c5b2-112">Finalización de llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="8c5b2-113">Conferencia de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="8c5b2-114">Reenvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="8c5b2-115">Llamada en espera</span><span class="sxs-lookup"><span data-stu-id="8c5b2-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="8c5b2-116">Detener llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="8c5b2-117">Recogida de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="8c5b2-118">Rechazar llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="8c5b2-119">Transferencia de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="8c5b2-120">Supervisión y recopilación de dígitos</span><span class="sxs-lookup"><span data-stu-id="8c5b2-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="8c5b2-121">Generar dígitos y tonos en banda</span><span class="sxs-lookup"><span data-stu-id="8c5b2-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="8c5b2-122">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="8c5b2-123">Control multimedia</span><span class="sxs-lookup"><span data-stu-id="8c5b2-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="8c5b2-124">Supervisión de medios</span><span class="sxs-lookup"><span data-stu-id="8c5b2-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="8c5b2-125">Servidores proxy</span><span class="sxs-lookup"><span data-stu-id="8c5b2-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="8c5b2-126">Calidad de servicio</span><span class="sxs-lookup"><span data-stu-id="8c5b2-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="8c5b2-127">Envío de información a una entidad remota</span><span class="sxs-lookup"><span data-stu-id="8c5b2-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="8c5b2-128">Administración de proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8c5b2-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="8c5b2-129">Configuración de un terminal para conversaciones telefónicas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="8c5b2-130">Supervisión de tonos</span><span class="sxs-lookup"><span data-stu-id="8c5b2-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="8c5b2-131">También hay [varias](#miscellaneous) funciones adicionales de servicio de línea.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="8c5b2-132">Modo y velocidad del portador</span><span class="sxs-lookup"><span data-stu-id="8c5b2-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="8c5b2-133">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-133">Function</span></span>                                       | <span data-ttu-id="8c5b2-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-135">**lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="8c5b2-136">Solicita un cambio en los parámetros de llamada de una llamada existente.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="8c5b2-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="8c5b2-138">Supervisión de medios</span><span class="sxs-lookup"><span data-stu-id="8c5b2-138">Media Monitoring</span></span>



| <span data-ttu-id="8c5b2-139">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-139">Function</span></span>                                     | <span data-ttu-id="8c5b2-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-141">**lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="8c5b2-142">Habilita o deshabilita la notificación del modo multimedia en una llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="8c5b2-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="8c5b2-144">Supervisión y recopilación de dígitos</span><span class="sxs-lookup"><span data-stu-id="8c5b2-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="8c5b2-145">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-145">Function</span></span>                                       | <span data-ttu-id="8c5b2-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-147">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="8c5b2-148">Habilita o deshabilita la notificación de detección de dígitos en una llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="8c5b2-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-149">Synchronous.</span></span> |
| [<span data-ttu-id="8c5b2-150">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="8c5b2-151">Realiza la recopilación de dígitos almacenada en búfer en una llamada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="8c5b2-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="8c5b2-153">Supervisión de tonos</span><span class="sxs-lookup"><span data-stu-id="8c5b2-153">Tone Monitoring</span></span>



| <span data-ttu-id="8c5b2-154">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-154">Function</span></span>                                     | <span data-ttu-id="8c5b2-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-156">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="8c5b2-157">Especifica qué tonos se deben detectar en una llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="8c5b2-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="8c5b2-159">Control multimedia</span><span class="sxs-lookup"><span data-stu-id="8c5b2-159">Media Control</span></span>



| <span data-ttu-id="8c5b2-160">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-160">Function</span></span>                                           | <span data-ttu-id="8c5b2-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-162">**lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="8c5b2-163">Configura el flujo multimedia de una llamada para el control multimedia.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="8c5b2-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="8c5b2-165">**lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="8c5b2-166">Establece los modos multimedia de la llamada especificada en su estructura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="8c5b2-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="8c5b2-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="8c5b2-168">Generar dígitos y tonos en banda</span><span class="sxs-lookup"><span data-stu-id="8c5b2-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="8c5b2-169">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-169">Function</span></span>                                         | <span data-ttu-id="8c5b2-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-171">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="8c5b2-172">Genera dígitos en banda en una llamada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-172">Generates inband digits on a call.</span></span> <span data-ttu-id="8c5b2-173">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-173">Synchronous.</span></span>               |
| [<span data-ttu-id="8c5b2-174">**lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="8c5b2-175">Genera un conjunto determinado de tonalidades inband en una llamada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="8c5b2-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="8c5b2-177">Llamar a Accept y Redirect</span><span class="sxs-lookup"><span data-stu-id="8c5b2-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="8c5b2-178">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-178">Function</span></span>                             | <span data-ttu-id="8c5b2-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-180">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="8c5b2-181">Acepta una llamada ofrecida e inicia alertas tanto del llamador (timbre) como de la entidad llamada (anillo).</span><span class="sxs-lookup"><span data-stu-id="8c5b2-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="8c5b2-182">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-182">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-183">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="8c5b2-184">Redirige una llamada de oferta a otra dirección.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="8c5b2-185">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="8c5b2-186">Rechazar llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-186">Call Reject</span></span>



| <span data-ttu-id="8c5b2-187">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-187">Function</span></span>                     | <span data-ttu-id="8c5b2-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-189">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="8c5b2-190">Desconecta una llamada o abandona un intento de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="8c5b2-191">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="8c5b2-192">Llamada en espera</span><span class="sxs-lookup"><span data-stu-id="8c5b2-192">Call Hold</span></span>



| <span data-ttu-id="8c5b2-193">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-193">Function</span></span>                         | <span data-ttu-id="8c5b2-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="8c5b2-195">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="8c5b2-196">Coloca la llamada especificada en suspensión.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="8c5b2-197">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-197">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-198">**lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="8c5b2-199">Recupera una llamada retenida.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-199">Retrieves a held call.</span></span> <span data-ttu-id="8c5b2-200">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="8c5b2-201">Protección de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-201">Securing Calls</span></span>



| <span data-ttu-id="8c5b2-202">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-202">Function</span></span>                                 | <span data-ttu-id="8c5b2-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-204">**lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="8c5b2-205">Protege una llamada existente de interferencias de otros eventos, como los pitidos en espera de llamadas en las conexiones de datos.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="8c5b2-206">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="8c5b2-207">Transferencia de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-207">Call Transfer</span></span>



| <span data-ttu-id="8c5b2-208">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-208">Function</span></span>                                             | <span data-ttu-id="8c5b2-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="8c5b2-211">Prepara una llamada especificada para la transferencia a otra dirección.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="8c5b2-212">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="8c5b2-213">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="8c5b2-214">Transfiere una llamada que se configuró para la transferencia a otra llamada o entra en una conferencia de tres vías.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="8c5b2-215">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-215">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-216">**lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="8c5b2-217">Transfiere una llamada a otra entidad.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-217">Transfers a call to another party.</span></span> <span data-ttu-id="8c5b2-218">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="8c5b2-219">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="8c5b2-220">Intercambia la llamada activa con la llamada actualmente en espera de consulta.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="8c5b2-221">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="8c5b2-222">Conferencia de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-222">Call Conference</span></span>



| <span data-ttu-id="8c5b2-223">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-223">Function</span></span>                                                         | <span data-ttu-id="8c5b2-224">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-225">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="8c5b2-226">Prepara una llamada determinada para la adición de otra entidad.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="8c5b2-227">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="8c5b2-228">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="8c5b2-229">Prepara para agregar una entidad a una llamada de conferencia existente colocando la llamada de conferencia en un estado de suspensión y creando una llamada de consulta que se puede agregar posteriormente a la llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="8c5b2-230">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-230">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-231">**lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="8c5b2-232">Agrega una llamada de consulta a una llamada de conferencia existente.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="8c5b2-233">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="8c5b2-234">**lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="8c5b2-235">Quita una entidad de una llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-235">Removes a party from a conference call.</span></span> <span data-ttu-id="8c5b2-236">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="8c5b2-237">Detener llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-237">Call Park</span></span>



| <span data-ttu-id="8c5b2-238">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-238">Function</span></span>                         | <span data-ttu-id="8c5b2-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="8c5b2-240">**linePark**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="8c5b2-241">Parques una llamada determinada en otra dirección.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-241">Parks a given call at another address.</span></span> <span data-ttu-id="8c5b2-242">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-242">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-243">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="8c5b2-244">Recupera una llamada deestacionada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-244">Retrieves a parked call.</span></span> <span data-ttu-id="8c5b2-245">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="8c5b2-246">Reenvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-246">Call Forwarding</span></span>



| <span data-ttu-id="8c5b2-247">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-247">Function</span></span>                           | <span data-ttu-id="8c5b2-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="8c5b2-249">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="8c5b2-250">Establece o cancela las solicitudes de reenvío de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="8c5b2-251">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="8c5b2-252">Recogida de llamadas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-252">Call Pickup</span></span>



| <span data-ttu-id="8c5b2-253">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-253">Function</span></span>                         | <span data-ttu-id="8c5b2-254">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-255">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="8c5b2-256">Recoge una alerta de llamada en una dirección de destino especificada y devuelve un identificador de llamada para la llamada de recogida ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) también se puede usar para la llamada en espera).</span><span class="sxs-lookup"><span data-stu-id="8c5b2-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="8c5b2-257">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="8c5b2-258">Envío de información a una entidad remota</span><span class="sxs-lookup"><span data-stu-id="8c5b2-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="8c5b2-259">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-259">Function</span></span>                                                   | <span data-ttu-id="8c5b2-260">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-261">**lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="8c5b2-262">Libera información de usuario del usuario, lo que permite al sistema sobrescribir este almacenamiento con información nueva.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="8c5b2-263">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-263">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-264">**lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="8c5b2-265">Envía información de usuario a la parte remota en la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="8c5b2-266">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="8c5b2-267">Finalización de llamada</span><span class="sxs-lookup"><span data-stu-id="8c5b2-267">Call Completion</span></span>



| <span data-ttu-id="8c5b2-268">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-268">Function</span></span>                                         | <span data-ttu-id="8c5b2-269">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="8c5b2-270">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="8c5b2-271">Coloca una solicitud de finalización de llamada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-271">Places a call completion request.</span></span> <span data-ttu-id="8c5b2-272">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="8c5b2-273">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="8c5b2-274">Cancela una solicitud de finalización de llamada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-274">Cancels a call completion request.</span></span> <span data-ttu-id="8c5b2-275">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="8c5b2-276">Configuración de un terminal para conversaciones telefónicas</span><span class="sxs-lookup"><span data-stu-id="8c5b2-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="8c5b2-277">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-277">Function</span></span>                                   | <span data-ttu-id="8c5b2-278">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-279">**lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="8c5b2-280">Especifica el dispositivo de terminal al que se enrutan los eventos de línea, eventos de dirección o secuencia de medios de llamada especificados.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="8c5b2-281">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="8c5b2-282">Prioridad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8c5b2-282">Application Priority</span></span>



| <span data-ttu-id="8c5b2-283">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-283">Function</span></span>                                         | <span data-ttu-id="8c5b2-284">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-285">**lineGetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="8c5b2-286">Recupera información de prioridad de telefonía de entrega o asistida para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="8c5b2-287">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-287">Synchronous.</span></span> |
| [<span data-ttu-id="8c5b2-288">**lineSetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="8c5b2-289">Establece la prioridad de entrega o de telefonía asistida para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="8c5b2-290">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="8c5b2-291">Administración de proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8c5b2-291">Service Provider Management</span></span>



| <span data-ttu-id="8c5b2-292">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-292">Function</span></span>                                           | <span data-ttu-id="8c5b2-293">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-294">**lineAddProvider**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="8c5b2-295">Instala un proveedor de servicios de telefonía.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-295">Installs a telephony service provider.</span></span> <span data-ttu-id="8c5b2-296">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="8c5b2-297">**lineConfigProvider**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="8c5b2-298">Muestra el cuadro de diálogo de configuración de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="8c5b2-299">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-299">Synchronous.</span></span> |
| [<span data-ttu-id="8c5b2-300">**lineRemoveProvider**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="8c5b2-301">Quita un proveedor de servicios de telefonía existente.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="8c5b2-302">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-302">Synchronous.</span></span>          |
| [<span data-ttu-id="8c5b2-303">**lineGetProviderList**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="8c5b2-304">Recupera una lista de proveedores de servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="8c5b2-305">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="8c5b2-306">Agentes</span><span class="sxs-lookup"><span data-stu-id="8c5b2-306">Agents</span></span>



| <span data-ttu-id="8c5b2-307">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-307">Function</span></span>                                                     | <span data-ttu-id="8c5b2-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-309">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="8c5b2-310">Permite a la aplicación tener acceso a funciones específicas del controlador del agente asociadas a la dirección.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="8c5b2-311">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-311">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-312">**lineGetAgentActivityList**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="8c5b2-313">Obtiene la lista de actividades de las que una aplicación selecciona las funciones que realiza un agente.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="8c5b2-314">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="8c5b2-315">**lineGetAgentCaps**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="8c5b2-316">Obtiene las capacidades relacionadas con el agente que se admiten en el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="8c5b2-317">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="8c5b2-318">**lineGetAgentGroupList**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="8c5b2-319">Obtiene la lista de grupos de agentes en los que un agente puede iniciar sesión en el distribuidor de llamadas automáticas.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="8c5b2-320">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="8c5b2-321">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="8c5b2-322">Obtiene el estado relacionado con el agente en la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="8c5b2-323">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="8c5b2-324">**lineSetAgentActivity**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="8c5b2-325">Establece el código de actividad del agente asociado a una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="8c5b2-326">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="8c5b2-327">**lineSetAgentGroup**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="8c5b2-328">Establece los grupos de agentes en los que el agente ha iniciado sesión en una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="8c5b2-329">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="8c5b2-330">**lineSetAgentState**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="8c5b2-331">Establece el estado del agente asociado a una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="8c5b2-332">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="8c5b2-333">Servidores proxy</span><span class="sxs-lookup"><span data-stu-id="8c5b2-333">Proxies</span></span>



| <span data-ttu-id="8c5b2-334">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-334">Function</span></span>                                       | <span data-ttu-id="8c5b2-335">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-336">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="8c5b2-337">Lo utiliza un controlador de solicitudes proxy registrado para generar mensajes TAPI.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="8c5b2-338">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-338">Synchronous.</span></span>  |
| [<span data-ttu-id="8c5b2-339">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="8c5b2-340">Indica la finalización de una solicitud de proxy por parte de un controlador proxy registrado.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="8c5b2-341">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="8c5b2-342">Calidad de servicio</span><span class="sxs-lookup"><span data-stu-id="8c5b2-342">Quality of Service</span></span>



| <span data-ttu-id="8c5b2-343">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-343">Function</span></span>                                                           | <span data-ttu-id="8c5b2-344">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-345">**lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="8c5b2-346">Solicita un cambio de los parámetros de calidad de servicio para una llamada existente.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="8c5b2-347">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="8c5b2-348">Varios</span><span class="sxs-lookup"><span data-stu-id="8c5b2-348">Miscellaneous</span></span>



| <span data-ttu-id="8c5b2-349">Función</span><span class="sxs-lookup"><span data-stu-id="8c5b2-349">Function</span></span>                                             | <span data-ttu-id="8c5b2-350">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5b2-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c5b2-351">**lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="8c5b2-352">Establece el miembro **CallData** de la estructura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="8c5b2-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="8c5b2-353">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-353">Asynchronous.</span></span> |
| [<span data-ttu-id="8c5b2-354">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="8c5b2-355">Establece los sonidos que el usuario oye cuando una llamada no tiene respuesta o está en espera.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="8c5b2-356">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="8c5b2-357">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="8c5b2-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="8c5b2-358">Establece el estado del dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="8c5b2-358">Sets the line device status.</span></span> <span data-ttu-id="8c5b2-359">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8c5b2-359">Asynchronous.</span></span>                                                            |



 

 

 



