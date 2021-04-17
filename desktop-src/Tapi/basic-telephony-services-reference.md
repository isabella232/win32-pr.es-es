---
description: Las funciones de telefonía básicas se enumeran por Categoría en las tablas siguientes.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Referencia de servicios de telefonía básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687253"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="49289-103">Referencia de servicios de telefonía básicos</span><span class="sxs-lookup"><span data-stu-id="49289-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="49289-104">Las funciones de telefonía básicas se enumeran por Categoría en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="49289-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="49289-105">Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje de respuesta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49289-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="49289-106">Si la función devuelve siempre su resultado a la aplicación inmediatamente, la función se considera [*sincrónica*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="49289-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="49289-107">A continuación se encuentra una agrupación funcional de las funciones básicas del servicio de telefonía:</span><span class="sxs-lookup"><span data-stu-id="49289-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="49289-108">Formatos de dirección</span><span class="sxs-lookup"><span data-stu-id="49289-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="49289-109">Direcciones</span><span class="sxs-lookup"><span data-stu-id="49289-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="49289-110">Responder a las llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="49289-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="49289-111">Llamar a funciones Drop</span><span class="sxs-lookup"><span data-stu-id="49289-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="49289-112">Manipulación de identificadores de llamadas</span><span class="sxs-lookup"><span data-stu-id="49289-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="49289-113">Llamar al control de privilegios</span><span class="sxs-lookup"><span data-stu-id="49289-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="49289-114">Estados de llamada y eventos</span><span class="sxs-lookup"><span data-stu-id="49289-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="49289-115">Estado y capacidades de línea</span><span class="sxs-lookup"><span data-stu-id="49289-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="49289-116">Negociación de la versión de línea</span><span class="sxs-lookup"><span data-stu-id="49289-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="49289-117">Información de ubicación y país o región</span><span class="sxs-lookup"><span data-stu-id="49289-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="49289-118">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="49289-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="49289-119">Dispositivos de línea de apertura y cierre</span><span class="sxs-lookup"><span data-stu-id="49289-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="49289-120">Solicitar servicios de destinatario</span><span class="sxs-lookup"><span data-stu-id="49289-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="49289-121">Inicialización y cierre de TAPI</span><span class="sxs-lookup"><span data-stu-id="49289-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="49289-122">Compatibilidad con el protector de peaje</span><span class="sxs-lookup"><span data-stu-id="49289-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="49289-123">Inicialización y cierre de TAPI</span><span class="sxs-lookup"><span data-stu-id="49289-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="49289-124">Función</span><span class="sxs-lookup"><span data-stu-id="49289-124">Function</span></span>                                     | <span data-ttu-id="49289-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-126">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="49289-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="49289-127">Inicializa la abstracción de línea TAPI para su uso por parte de la aplicación que invoca.</span><span class="sxs-lookup"><span data-stu-id="49289-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="49289-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-128">Synchronous.</span></span> |
| [<span data-ttu-id="49289-129">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="49289-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="49289-130">Cierra el uso de la aplicación de la abstracción de línea de TAPI.</span><span class="sxs-lookup"><span data-stu-id="49289-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="49289-131">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="49289-132">Negociación de la versión de línea</span><span class="sxs-lookup"><span data-stu-id="49289-132">Line Version Negotiation</span></span>



| <span data-ttu-id="49289-133">Función</span><span class="sxs-lookup"><span data-stu-id="49289-133">Function</span></span>                                                   | <span data-ttu-id="49289-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="49289-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="49289-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="49289-136">Permite a una aplicación negociar una versión de TAPI para usarla.</span><span class="sxs-lookup"><span data-stu-id="49289-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="49289-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="49289-138">Estado y capacidades de línea</span><span class="sxs-lookup"><span data-stu-id="49289-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="49289-139">Función</span><span class="sxs-lookup"><span data-stu-id="49289-139">Function</span></span>                                               | <span data-ttu-id="49289-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-141">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="49289-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="49289-142">Devuelve las capacidades de un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="49289-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="49289-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="49289-144">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="49289-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="49289-145">Devuelve la configuración de un dispositivo de flujo de multimedia.</span><span class="sxs-lookup"><span data-stu-id="49289-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="49289-146">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="49289-147">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="49289-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="49289-148">Devuelve el estado actual del dispositivo de línea abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="49289-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="49289-150">**lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="49289-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="49289-151">Establece la configuración del dispositivo de flujo multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="49289-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="49289-153">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="49289-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="49289-154">Especifica los cambios de estado para los que se debe notificar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49289-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="49289-155">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="49289-156">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="49289-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="49289-157">Devuelve la configuración de mensajes de estado de dirección y línea actual de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49289-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="49289-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="49289-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="49289-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="49289-160">Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas.</span><span class="sxs-lookup"><span data-stu-id="49289-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="49289-161">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="49289-162">**lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="49289-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="49289-163">Permite que una aplicación recupere un icono para mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="49289-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="49289-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="49289-165">**lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="49289-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="49289-166">Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="49289-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="49289-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-167">Synchronous.</span></span> |
| [<span data-ttu-id="49289-168">**lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="49289-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="49289-169">Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="49289-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="49289-170">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="49289-171">Direcciones</span><span class="sxs-lookup"><span data-stu-id="49289-171">Addresses</span></span>



| <span data-ttu-id="49289-172">Función</span><span class="sxs-lookup"><span data-stu-id="49289-172">Function</span></span>                                             | <span data-ttu-id="49289-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-174">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="49289-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="49289-175">Devuelve las capacidades de telefonía de una dirección.</span><span class="sxs-lookup"><span data-stu-id="49289-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="49289-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="49289-177">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="49289-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="49289-178">Devuelve el estado actual de una dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="49289-178">Returns current status of a specified address.</span></span> <span data-ttu-id="49289-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="49289-180">**lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="49289-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="49289-181">Recupera el identificador de dirección de una dirección especificada con un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="49289-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="49289-182">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="49289-183">Dispositivos de línea de apertura y cierre</span><span class="sxs-lookup"><span data-stu-id="49289-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="49289-184">Función</span><span class="sxs-lookup"><span data-stu-id="49289-184">Function</span></span>                       | <span data-ttu-id="49289-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="49289-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="49289-187">Abre un dispositivo de línea especificado para proporcionar una supervisión o control posterior de la línea.</span><span class="sxs-lookup"><span data-stu-id="49289-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="49289-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-188">Synchronous.</span></span> |
| [<span data-ttu-id="49289-189">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="49289-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="49289-190">Cierra un dispositivo de línea abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-190">Closes a specified opened line device.</span></span> <span data-ttu-id="49289-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="49289-192">Formatos de dirección</span><span class="sxs-lookup"><span data-stu-id="49289-192">Address Formats</span></span>



| <span data-ttu-id="49289-193">Función</span><span class="sxs-lookup"><span data-stu-id="49289-193">Function</span></span>                                                 | <span data-ttu-id="49289-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-195">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="49289-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="49289-196">Traduce entre una dirección en formato canónico y una dirección en formato de marcado.</span><span class="sxs-lookup"><span data-stu-id="49289-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="49289-197">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-197">Synchronous.</span></span> |
| [<span data-ttu-id="49289-198">**lineSetCurrentLocation**</span><span class="sxs-lookup"><span data-stu-id="49289-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="49289-199">Establece la ubicación usada como contexto para la traducción de direcciones.</span><span class="sxs-lookup"><span data-stu-id="49289-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="49289-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="49289-201">**lineSetTollList**</span><span class="sxs-lookup"><span data-stu-id="49289-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="49289-202">Manipula la lista de llamadas.</span><span class="sxs-lookup"><span data-stu-id="49289-202">Manipulates the toll list.</span></span> <span data-ttu-id="49289-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="49289-204">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="49289-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="49289-205">Devuelve capacidades de traducción de direcciones.</span><span class="sxs-lookup"><span data-stu-id="49289-205">Returns address translation capabilities.</span></span> <span data-ttu-id="49289-206">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="49289-207">Estados de llamada y eventos</span><span class="sxs-lookup"><span data-stu-id="49289-207">Call States and Events</span></span>



| <span data-ttu-id="49289-208">Función</span><span class="sxs-lookup"><span data-stu-id="49289-208">Function</span></span>                                         | <span data-ttu-id="49289-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-210">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="49289-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="49289-211">Devuelve información fija sobre una llamada.</span><span class="sxs-lookup"><span data-stu-id="49289-211">Returns fixed information about a call.</span></span> <span data-ttu-id="49289-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="49289-213">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="49289-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="49289-214">Devuelve información completa del estado de la llamada de la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="49289-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="49289-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-215">Synchronous.</span></span>       |
| [<span data-ttu-id="49289-216">**lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="49289-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="49289-217">Establece el campo específico de la aplicación de la estructura de información de una llamada.</span><span class="sxs-lookup"><span data-stu-id="49289-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="49289-218">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="49289-219">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="49289-219">Making Calls</span></span>



| <span data-ttu-id="49289-220">Función</span><span class="sxs-lookup"><span data-stu-id="49289-220">Function</span></span>                             | <span data-ttu-id="49289-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="49289-222">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="49289-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="49289-223">Realiza una llamada saliente y devuelve un identificador de llamada para ella.</span><span class="sxs-lookup"><span data-stu-id="49289-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="49289-224">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="49289-224">Asynchronous.</span></span> |
| [<span data-ttu-id="49289-225">**Fino**</span><span class="sxs-lookup"><span data-stu-id="49289-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="49289-226">Dials (partes de una o varias direcciones marcables).</span><span class="sxs-lookup"><span data-stu-id="49289-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="49289-227">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="49289-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="49289-228">Responder a las llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="49289-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="49289-229">Función</span><span class="sxs-lookup"><span data-stu-id="49289-229">Function</span></span>                         | <span data-ttu-id="49289-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="49289-231">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="49289-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="49289-232">Responde a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="49289-232">Answers an incoming call.</span></span> <span data-ttu-id="49289-233">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="49289-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="49289-234">Compatibilidad con el protector de peaje</span><span class="sxs-lookup"><span data-stu-id="49289-234">Toll Saver Support</span></span>



| <span data-ttu-id="49289-235">Función</span><span class="sxs-lookup"><span data-stu-id="49289-235">Function</span></span>                                   | <span data-ttu-id="49289-236">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-237">**lineSetNumRings**</span><span class="sxs-lookup"><span data-stu-id="49289-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="49289-238">Indica el número de anillos después del cual se responderá a las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="49289-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="49289-239">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="49289-240">**lineGetNumRings**</span><span class="sxs-lookup"><span data-stu-id="49289-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="49289-241">Devuelve el número mínimo de anillos solicitados con [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span><span class="sxs-lookup"><span data-stu-id="49289-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="49289-242">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="49289-243">Llamar al control de privilegios</span><span class="sxs-lookup"><span data-stu-id="49289-243">Call Privilege Control</span></span>



| <span data-ttu-id="49289-244">Función</span><span class="sxs-lookup"><span data-stu-id="49289-244">Function</span></span>                                             | <span data-ttu-id="49289-245">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="49289-246">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="49289-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="49289-247">Establece el privilegio de la aplicación en el privilegio especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="49289-248">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="49289-249">Llamar a funciones Drop</span><span class="sxs-lookup"><span data-stu-id="49289-249">Call Drop Functions</span></span>



| <span data-ttu-id="49289-250">Función</span><span class="sxs-lookup"><span data-stu-id="49289-250">Function</span></span>                                         | <span data-ttu-id="49289-251">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="49289-252">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="49289-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="49289-253">Desconecta una llamada o abandona un intento de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="49289-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="49289-254">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="49289-254">Asynchronous.</span></span> |
| [<span data-ttu-id="49289-255">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="49289-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="49289-256">Desasigna el identificador de llamada especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="49289-257">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="49289-258">Manipulación de identificadores de llamadas</span><span class="sxs-lookup"><span data-stu-id="49289-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="49289-259">Función</span><span class="sxs-lookup"><span data-stu-id="49289-259">Function</span></span>                                                   | <span data-ttu-id="49289-260">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-261">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="49289-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="49289-262">La entrega de la llamada a la propiedad y/o cambia los privilegios de una aplicación a una llamada.</span><span class="sxs-lookup"><span data-stu-id="49289-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="49289-263">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="49289-264">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="49289-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="49289-265">Devuelve los identificadores de llamada a las llamadas en una línea o dirección especificada para los que la aplicación todavía no tiene identificadores.</span><span class="sxs-lookup"><span data-stu-id="49289-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="49289-266">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-266">Synchronous.</span></span> |
| [<span data-ttu-id="49289-267">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="49289-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="49289-268">Devuelve una lista de identificadores de llamada que forman parte de la misma llamada de conferencia que la llamada especificada como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="49289-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="49289-269">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="49289-270">Información de ubicación y país o región</span><span class="sxs-lookup"><span data-stu-id="49289-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="49289-271">Función</span><span class="sxs-lookup"><span data-stu-id="49289-271">Function</span></span>                                           | <span data-ttu-id="49289-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-273">**lineTranslateDialog**</span><span class="sxs-lookup"><span data-stu-id="49289-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="49289-274">Muestra un cuadro de diálogo que permite al usuario cambiar la ubicación y la información de la tarjeta de llamada.</span><span class="sxs-lookup"><span data-stu-id="49289-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="49289-275">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-275">Synchronous.</span></span> |
| [<span data-ttu-id="49289-276">**lineGetCountry**</span><span class="sxs-lookup"><span data-stu-id="49289-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="49289-277">Recupera las reglas de marcado y otra información acerca de un país o región determinados.</span><span class="sxs-lookup"><span data-stu-id="49289-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="49289-278">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="49289-279">Solicitar servicios de destinatario</span><span class="sxs-lookup"><span data-stu-id="49289-279">Request Recipient Services</span></span>

<span data-ttu-id="49289-280">Las dos funciones siguientes solo se usan para admitir la telefonía asistida.</span><span class="sxs-lookup"><span data-stu-id="49289-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="49289-281">Función</span><span class="sxs-lookup"><span data-stu-id="49289-281">Function</span></span>                                                             | <span data-ttu-id="49289-282">Descripción</span><span class="sxs-lookup"><span data-stu-id="49289-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49289-283">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="49289-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="49289-284">Registra o anula el registro de la aplicación como un destinatario de la solicitud para el modo de solicitud especificado.</span><span class="sxs-lookup"><span data-stu-id="49289-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="49289-285">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-285">Synchronous.</span></span> |
| [<span data-ttu-id="49289-286">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="49289-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="49289-287">Obtiene la solicitud siguiente de la biblioteca de vínculos dinámicos de telefonía.</span><span class="sxs-lookup"><span data-stu-id="49289-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="49289-288">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49289-288">Synchronous.</span></span>                                  |



 

 

 



