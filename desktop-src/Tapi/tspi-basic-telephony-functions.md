---
description: Todos los proveedores de servicios deben implementar funciones de telefonía básicas.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funciones de telefonía básicas de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913217"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="8f9f7-103">Funciones de telefonía básicas de TSPI</span><span class="sxs-lookup"><span data-stu-id="8f9f7-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="8f9f7-104">Todos los proveedores de servicios deben implementar funciones de telefonía básicas.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="8f9f7-105">A continuación se muestra una lista de estas funciones por categoría.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="8f9f7-106">Una función se identifica como *asincrónica* si indica la finalización en un mensaje de respuesta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="8f9f7-107">Si la función devuelve siempre su resultado inmediatamente, la función se considera *sincrónica*.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="8f9f7-108">Direcciones</span><span class="sxs-lookup"><span data-stu-id="8f9f7-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="8f9f7-109">Responder a las llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="8f9f7-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="8f9f7-110">Llamar a funciones Drop</span><span class="sxs-lookup"><span data-stu-id="8f9f7-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="8f9f7-111">Estados de llamada y eventos</span><span class="sxs-lookup"><span data-stu-id="8f9f7-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="8f9f7-112">Estado y capacidades de línea</span><span class="sxs-lookup"><span data-stu-id="8f9f7-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="8f9f7-113">Negociación de la versión de línea</span><span class="sxs-lookup"><span data-stu-id="8f9f7-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="8f9f7-114">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="8f9f7-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="8f9f7-115">Dispositivos de línea de apertura y cierre</span><span class="sxs-lookup"><span data-stu-id="8f9f7-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="8f9f7-116">Negociación de la versión de teléfono</span><span class="sxs-lookup"><span data-stu-id="8f9f7-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="8f9f7-117">Inicialización y cierre de TSP</span><span class="sxs-lookup"><span data-stu-id="8f9f7-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="8f9f7-118">Inicialización y cierre de TSP</span><span class="sxs-lookup"><span data-stu-id="8f9f7-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="8f9f7-119">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="8f9f7-120">Instala un TSP.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-120">Installs a TSP.</span></span> <span data-ttu-id="8f9f7-121">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="8f9f7-122">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="8f9f7-123">Instala el TSP.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-123">Installs the TSP.</span></span> <span data-ttu-id="8f9f7-124">Obsoleto con la versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="8f9f7-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-125">Synchronous.</span></span> |
| [<span data-ttu-id="8f9f7-126">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="8f9f7-127">Inicializa el TSP.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-127">Initializes the TSP.</span></span> <span data-ttu-id="8f9f7-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="8f9f7-129">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="8f9f7-130">Cierra el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="8f9f7-131">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="8f9f7-132">Quita un TSP.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-132">Removes a TSP.</span></span> <span data-ttu-id="8f9f7-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="8f9f7-134">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="8f9f7-135">Quita un TSP.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-135">Removes a TSP.</span></span> <span data-ttu-id="8f9f7-136">Obsoleto con la versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="8f9f7-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="8f9f7-138">Negociación de la versión de teléfono</span><span class="sxs-lookup"><span data-stu-id="8f9f7-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-139">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="8f9f7-140">Devuelve la versión de SPI más alta en la que el proveedor de servicios puede operar para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="8f9f7-141">Negociación de la versión de línea</span><span class="sxs-lookup"><span data-stu-id="8f9f7-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-142">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="8f9f7-143">Permite que una aplicación negocie una versión de TSPI para usarla con un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="8f9f7-144">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="8f9f7-145">Estado y capacidades de línea</span><span class="sxs-lookup"><span data-stu-id="8f9f7-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-146">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="8f9f7-147">Devuelve las capacidades de un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="8f9f7-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="8f9f7-149">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="8f9f7-150">Devuelve la configuración de un dispositivo de flujo de multimedia.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="8f9f7-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="8f9f7-152">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="8f9f7-153">Devuelve el estado actual del dispositivo de línea abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="8f9f7-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="8f9f7-155">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="8f9f7-156">Establece la configuración del dispositivo de flujo multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="8f9f7-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="8f9f7-158">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="8f9f7-159">Especifica los cambios de estado para los que se debe notificar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="8f9f7-160">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="8f9f7-161">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="8f9f7-162">Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="8f9f7-163">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="8f9f7-164">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="8f9f7-165">Permite que una aplicación recupere un icono para mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="8f9f7-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="8f9f7-167">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="8f9f7-168">Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="8f9f7-169">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-169">Synchronous.</span></span> |
| [<span data-ttu-id="8f9f7-170">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="8f9f7-171">Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="8f9f7-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="8f9f7-173">Direcciones</span><span class="sxs-lookup"><span data-stu-id="8f9f7-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-174">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="8f9f7-175">Devuelve las capacidades de telefonía de una dirección.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="8f9f7-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="8f9f7-177">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="8f9f7-178">Devuelve el estado actual de una dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-178">Returns current status of a specified address.</span></span> <span data-ttu-id="8f9f7-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="8f9f7-180">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="8f9f7-181">Recupera el número de identificadores de dirección admitidos en la línea indicada.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="8f9f7-182">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="8f9f7-183">Recupera el identificador de dirección de una dirección especificada con un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="8f9f7-184">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="8f9f7-185">Dispositivos de línea de apertura y cierre</span><span class="sxs-lookup"><span data-stu-id="8f9f7-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-186">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="8f9f7-187">Abre un dispositivo de línea especificado para proporcionar una supervisión o control posterior de la línea.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="8f9f7-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-188">Synchronous.</span></span> |
| [<span data-ttu-id="8f9f7-189">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="8f9f7-190">Cierra un dispositivo de línea abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-190">Closes a specified opened line device.</span></span> <span data-ttu-id="8f9f7-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="8f9f7-192">Estados de llamada y eventos</span><span class="sxs-lookup"><span data-stu-id="8f9f7-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-193">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="8f9f7-194">Devuelve información fija sobre una llamada.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-194">Returns fixed information about a call.</span></span> <span data-ttu-id="8f9f7-195">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="8f9f7-196">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="8f9f7-197">Devuelve información completa del estado de la llamada de la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="8f9f7-198">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-198">Synchronous.</span></span>       |
| [<span data-ttu-id="8f9f7-199">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="8f9f7-200">Establece el campo específico de la aplicación de la estructura de información de una llamada.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="8f9f7-201">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="8f9f7-202">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="8f9f7-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-203">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="8f9f7-204">Realiza una llamada saliente y devuelve un identificador de llamada para ella.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="8f9f7-205">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8f9f7-205">Asynchronous.</span></span> |
| [<span data-ttu-id="8f9f7-206">**TSPI \_ alineado**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="8f9f7-207">Dials (partes de una o varias direcciones marcables).</span><span class="sxs-lookup"><span data-stu-id="8f9f7-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="8f9f7-208">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8f9f7-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="8f9f7-209">Responder a las llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="8f9f7-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="8f9f7-210">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="8f9f7-211">Responde a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-211">Answers an incoming call.</span></span> <span data-ttu-id="8f9f7-212">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8f9f7-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="8f9f7-213">Llamar a funciones Drop</span><span class="sxs-lookup"><span data-stu-id="8f9f7-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f7-214">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="8f9f7-215">Desconecta una llamada o abandona un intento de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="8f9f7-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="8f9f7-216">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="8f9f7-216">Asynchronous.</span></span> |



 

 

 
